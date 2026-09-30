# Floodgate Companion
a Companion Plugin for floodgate that fetches Link informations and helps you choose save data!
Requires Geyser And Floodgate to load the Bedrock UI
> [!NOTE]
> Note: Geyser Standalone is Not Supported! Use Waterfall / Velocity Instead if you dont want to install Geyser on the server itself!
> Not only that, we recommend you to run the latest version if you are using Waterfall / Velocity and use for bungeecord: BungeeViaProxy or for Velocity: Direct ViaVersion and [AspirinConnect](https://github.com/creeper123123321/VIAaaS-UI)

# How Does it work

## User data
Let's use My Friend's Information For Demo.

| Username | UUID | Connected From | Skin |
|-|-|-|-|
|.MinuteLoby|00000000-0000-0000-0009-01fc0acf49f9|Minecraft4Windows|<img width="100" height="106" alt="image" src="https://github.com/user-attachments/assets/cf6a145c-2e33-49cb-bdff-37cf7ae681a7" />

| Username | UUID | Connected From | Skin |
|-|-|-|-|
|Soji_Lab|86c00938-9011-43ee-9a46-14fc714840d3|Minecraft Java Edition|<img width="100" height="106" alt="image" src="https://github.com/user-attachments/assets/33a4ba1d-b47d-425c-a75c-ceb82987a36f" />

This is Before Linking.

| Username | UUID | Connected From | Skin |
|-|-|-|-|
|Soji_Lab|86c00938-9011-43ee-9a46-14fc714840d3|Minecraft4Windows|<img width="100" height="106" alt="image" src="https://github.com/user-attachments/assets/33a4ba1d-b47d-425c-a75c-ceb82987a36f" />

This is After Linking. as you can see, her/his Data was overriden by GeyserMC Link System.

## First Join
```
[00:08:12 INFO]: [Geyser-Spigot] 플레이어가 사용자명 MinuteLoby (1234)(으)로 연결했습니다.
[00:08:12 INFO]: [Geyser-Spigot] MinuteLoby (MinuteLoby로 로그인) (이)가 Java 서버에 접속했습니다
[00:08:12 INFO]: [FloodgateCompanion] MinuteLoby's XUID is 2535456815139321. Checking Linked Status...
[00:08:12 INFO]: [FloodgateCompanion] Link Detected! Creating Both Java & Bedrock Data
[00:08:12 INFO]: [FloodgateCompanion] Java: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / Bedrock: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] Waiting for User Selection...
```
## Only Bedrock Data Exist
```
[00:08:12 INFO]: [Geyser-Spigot] 플레이어가 사용자명 MinuteLoby (1234)(으)로 연결했습니다.
[00:08:12 INFO]: [Geyser-Spigot] MinuteLoby (MinuteLoby로 로그인) (이)가 Java 서버에 접속했습니다
[00:08:12 INFO]: [FloodgateCompanion] MinuteLoby's XUID is 2535456815139321. Checking Linked Status...
[00:08:12 INFO]: [FloodgateCompanion] Link Detected! Creating Both Java & Bedrock Data
[00:08:12 INFO]: [FloodgateCompanion] Bedrock Data Already Exists. Only Creating Java.
[00:08:12 INFO]: [FloodgateCompanion] Java: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / Bedrock: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] Waiting for User Selection...
```
## Only Java Data Exist
```
[00:08:12 INFO]: [Geyser-Spigot] 플레이어가 사용자명 MinuteLoby (1234)(으)로 연결했습니다.
[00:08:12 INFO]: [Geyser-Spigot] MinuteLoby (MinuteLoby로 로그인) (이)가 Java 서버에 접속했습니다
[00:08:12 INFO]: [FloodgateCompanion] MinuteLoby's XUID is 2535456815139321. Checking Linked Status...
[00:08:12 INFO]: [FloodgateCompanion] Link Detected! Creating Both Java & Bedrock Data
[00:08:12 INFO]: [FloodgateCompanion] Java Data Already Exists. Only Creating Bedrock.
[00:08:12 INFO]: [FloodgateCompanion] Java: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / Bedrock: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] Waiting for User Selection...
```
## Both Data Exist
```
[00:08:12 INFO]: [Geyser-Spigot] 플레이어가 사용자명 MinuteLoby (1234)(으)로 연결했습니다.
[00:08:12 INFO]: [Geyser-Spigot] MinuteLoby (MinuteLoby로 로그인) (이)가 Java 서버에 접속했습니다
[00:08:12 INFO]: [FloodgateCompanion] MinuteLoby's XUID is 2535456815139321. Checking Linked Status...
[00:08:12 INFO]: [FloodgateCompanion] Link Detected! Creating Both Java & Bedrock Data
[00:08:12 INFO]: [FloodgateCompanion] Both Data Exists. Skipping Data Creation.
[00:08:12 INFO]: [FloodgateCompanion] Java: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / Bedrock: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] Waiting for User Selection...
```

## Data Selection Confirmation (Bedrock)
```
[00:08:12 INFO]: [FloodgateCompanion] Link Detected! Creating Both Java & Bedrock Data
[00:08:12 INFO]: [FloodgateCompanion] Both Data Exists. Skipping.
[00:08:12 INFO]: [FloodgateCompanion] Java: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / Bedrock: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] Waiting for User Selection...
[00:08:14 INFO]: [FloodgateCompanion] MinuteLoby Has Selected Java Data: Joining as Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3)
[00:08:14 INFO]: [floodgate] Soji_Lab(으)로 로그인된 Floodgate 플레이어가 참여했습니다 (UUID: 86c00938-9011-43ee-9a46-14fc714840d3}
[00:08:14 INFO]: Soji_Lab[/???.???.???.???:0] logged in with entity id 123 45 678 at ([minecraft:overworld])
[00:08:14 INFO]: 입장 | [자바에디션유저]소지님이 입장했습니다.
```

## Data Selection Confirmation (Java)
```
[00:08:12 INFO]: [FloodgateCompanion] Link Detected! Creating Both Java & Bedrock Data
[00:08:12 INFO]: [FloodgateCompanion] Both Data Exists. Skipping.
[00:08:12 INFO]: [FloodgateCompanion] Java: Soji_Lab(UUID: 86c00938-9011-43ee-9a46-14fc714840d3) / Bedrock: .MinuteLoby (UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:12 INFO]: [FloodgateCompanion] Waiting for User Selection...
[00:08:14 INFO]: [FloodgateCompanion] MinuteLoby Has Selected Bedrock Data: Joining as .MinuteLoby(UUID: 00000000-0000-0000-0009-01fc0acf49f9)
[00:08:14 INFO]: [floodgate] Soji_Lab(으)로 로그인된 Floodgate 플레이어가 참여했습니다 (UUID: 00000000-0000-0000-0009-01fc0acf49f9}
[00:08:14 INFO]: .MinuteLoby[/???.???.???.???:0] logged in with entity id 123 45 678 at ([minecraft:overworld])
[00:08:14 INFO]: 입장 | [포켓에디션유저]소지님이 입장했습니다.
```
# MinekubeConnect Support
> [!CAUTION]
> This function is Not Yet Available due to Minekube's internal system limitation(The Test server in MineKube Mode also requires Java Edition Account Linked Bedrock Edition Account).

the Floodgate Companion will also Manipulate the User's Username Back from underscore with spaces UUIDv5 to userspecified prefix with spaces username with 0 padding UUID.

for example:

| Username | UUID | Connected From | Skin |
|-|-|-|-|
|_MinuteLoby|51b7ae26-2a21-4452-b70f-97cc9598e475|MinekubeConnect+Minecraft4Windows|<img width="180" height="191" alt="image" src="https://github.com/user-attachments/assets/8cce1ef7-531e-4d0b-b6d1-c6503b119b27" />

is Manipulated Back to

| Username | UUID | Connected From | Skin |
|-|-|-|-|
|.MinuteLoby|00000000-0000-0000-0009-01fc0acf49f9|MinekubeConnect+Minecraft4Windows|<img width="180" height="191" alt="image" src="https://github.com/user-attachments/assets/8cce1ef7-531e-4d0b-b6d1-c6503b119b27" />

TO use tebex, you need to turn on use-Minekube-username. However, in south korea. making LLC(Liability Limited Company) is Recommended over the Tebex. LLC is much safer because it will be Legal Entity in form of Sole proprietor.

