# Floodgate Companion
베드락 에디션 계정 선택을 가능하게 해주는 Floodgate 보조 플러그인입니다.
Bedrock UI를 사용하시려면 Geyser와 Floodgate가 설치되어있어야 합니다. 지원하지 않는 경우, Java UI로만 표시됩니다.
> [!NOTE]
> 단독사용하는 Geyser는 지원하지 않습니다! Geyser, Floodgate를 서버에 설치하고 싶지 않으신 경우 Waterfall / Velocity을 대신 사용해주십시오.
> Waterfall / Velocity를 최신 버전으로 써주시고 번지코드 사용중이시라면: BungeeViaProxy를 사용하거나 벨로시티 사용시 ViaVersion을 프록시서버에 넣거나 서버가 외부에서 구동되는 경우 [AspirinConnect](https://github.com/creeper123123321/VIAaaS-UI)를 사용하실 수 있습니다.

# 작동원리

## 유저 데이터
제 친구 소지님의 예시를 들어보겠습니다. (참고로 제가 바니팜에서 만난 친구입니다)

| 사용자명 | UUID | 사용된 클라이언트 | 스킨 |
|-|-|-|-|
|.MinuteLoby|00000000-0000-0000-0009-01fc0acf49f9|Windows 전용 마크 포켓 에디션|<img width="100" height="106" alt="image" src="https://github.com/user-attachments/assets/cf6a145c-2e33-49cb-bdff-37cf7ae681a7" />

| 사용자명 | UUID | 사용된 클라이언트 | 스킨 |
|-|-|-|-|
|Soji_Lab|86c00938-9011-43ee-9a46-14fc714840d3|Windows 전용 마크 자바 에디션|<img width="100" height="106" alt="image" src="https://github.com/user-attachments/assets/33a4ba1d-b47d-425c-a75c-ceb82987a36f" />

연동 이전 프로필입니다.

| 사용자명 | UUID | 사용된 클라이언트 | 스킨 |
|-|-|-|-|
|Soji_Lab|86c00938-9011-43ee-9a46-14fc714840d3|Windows 전용 마크 포켓 에디션|<img width="100" height="106" alt="image" src="https://github.com/user-attachments/assets/33a4ba1d-b47d-425c-a75c-ceb82987a36f" />

연동 이후 프로필입니다. 보셨다시피, 소지님의 프로필이 자바 에디션 계정으로 합쳐졌기 때문에 포켓 에디션 계정 데이터를 불러오지 않습니다. 부계정 방지 플러그인과 충돌할 수 있는 위험한 상황입니다.

이 플러그인을 설치하여 해결할 수 있습니다.

## 서버 참여
```
[00:08:12 INFO]: [Geyser-Spigot] 플레이어가 사용자명 MinuteLoby (1234)(으)로 연결했습니다.
[00:08:12 INFO]: [Geyser-Spigot] MinuteLoby (MinuteLoby로 로그인) (이)가 Java 서버에 접속했습니다
[00:08:12 INFO]: [FloodgateCompanion] MinuteLoby님의 XUID는 2535456815139321입니다. 연동 상태 확인 중입니다...
[00:08:12 INFO]: [FloodgateCompanion] 연동 확인! (연동된 JE 계정은 Soji_Lab 입니다.)
[00:08:12 INFO]: [FloodgateCompanion] JE: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / BE: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] 유저 선택 대기 중입니다...
```

## 데이터 선택 확인 (Java)
```
[00:08:12 INFO]: [FloodgateCompanion] 연동 확인!
[00:08:12 INFO]: [FloodgateCompanion] JE: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / BE: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] 유저 선택 대기 중입니다...
[00:08:14 INFO]: [FloodgateCompanion] MinuteLoby님이 Java Edition 로그인을 선택했습니다. Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) 계정으로 로그인합니다.
[00:08:14 INFO]: [floodgate] Soji_Lab(으)로 로그인된 Floodgate 플레이어가 참여했습니다 (UUID: 86c00938-9011-43ee-9a46-14fc714840d3}
[00:08:14 INFO]: Soji_Lab[/???.???.???.???:0] logged in with entity id 123 45 678 at ([minecraft:overworld])
[00:08:14 INFO]: 입장 | [자바에디션유저]소지님이 입장했습니다.
```

## 데이터 선택 확인 (Bedrock)
```
[00:08:12 INFO]: [FloodgateCompanion] 연동 확인!
[00:08:12 INFO]: [FloodgateCompanion] 자바에디션: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / 포켓에디션: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] 유저 선택 대기 중입니다...
[00:08:14 INFO]: [FloodgateCompanion] MinuteLoby님이 Bedrock Edition 로그인을 선택했습니다. .MinuteLoby(UUID: 00000000-0000-0000-0009-01fc0acf49f9) 계정으로 로그인합니다.
[00:08:14 INFO]: [floodgate] .MinuteLoby(으)로 로그인된 Floodgate 플레이어가 참여했습니다 (UUID: 00000000-0000-0000-0009-01fc0acf49f9}
[00:08:14 INFO]: .MinuteLoby[/???.???.???.???:0] logged in with entity id 123 45 678 at ([minecraft:overworld])
[00:08:14 INFO]: 입장 | [포켓에디션유저]소지님이 입장했습니다.
```
# MinekubeConnect 지원

ConnectCompanion은 베드락 유저 UUID, 유저네임을 Floodgate 표준 양식으로 변경합니다.

예제:

| Username | UUID | Connected From | Skin |
|-|-|-|-|
|_MinuteLoby|51b7ae26-2a21-4452-b70f-97cc9598e475|MinekubeConnect+Minecraft4Windows|<img width="180" height="191" alt="image" src="https://github.com/user-attachments/assets/8cce1ef7-531e-4d0b-b6d1-c6503b119b27" />

데이터가

| Username | UUID | Connected From | Skin |
|-|-|-|-|
|.MinuteLoby|00000000-0000-0000-0009-01fc0acf49f9|MinekubeConnect+Minecraft4Windows|<img width="180" height="191" alt="image" src="https://github.com/user-attachments/assets/8cce1ef7-531e-4d0b-b6d1-c6503b119b27" />

로 되돌아옵니다.

```
[00:08:12 INFO]: [ConnectCompanion] /???.???.???.???에서 Connect 접속을 시도하였습니다!
[00:08:12 INFO]: [ConnectCompanion] Connect 이용 중인 플레이어가 PE 사용자명 MinuteLoby (1234)(으)로 연결했습니다.
[00:08:12 INFO]: [ConnectCompanion] PE: MinuteLoby님의 XUID는 2535456815139321입니다. 호환 UUID(00000000-0000-0000-XUID-HEXADECVALUE)를 생성합니다.
[00:08:12 INFO]: [FloodgateCompanion] 연동 확인! (연동된 JE 계정은 Soji_Lab 입니다.)
[00:08:12 INFO]: [FloodgateCompanion] JE: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / BE: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] 유저 선택 대기 중입니다...
[00:08:12 INFO]: [FloodgateCompanion] 연동 확인!
[00:08:12 INFO]: [FloodgateCompanion] 자바에디션: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / 포켓에디션: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] 유저 선택 대기 중입니다...
[00:08:14 INFO]: [FloodgateCompanion] MinuteLoby님이 Bedrock Edition 로그인을 선택했습니다. .MinuteLoby(UUID: 00000000-0000-0000-0009-01fc0acf49f9) 계정으로 로그인합니다.
[00:08:14 INFO]: [floodgate] .MinuteLoby(으)로 로그인된 Floodgate 플레이어가 참여했습니다 (UUID: 00000000-0000-0000-0009-01fc0acf49f9}
[00:08:14 INFO]: .MinuteLoby[/???.???.???.???:0] logged in with entity id 123 45 678 at ([minecraft:overworld])
[00:08:14 INFO]: 입장 | [포켓에디션유저]소지님이 입장했습니다.
```
