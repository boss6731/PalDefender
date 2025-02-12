### [<<<](../README_ZH_TW.md) Wiki

#### [English](./README.md) / 繁體中文

# 命令

### 目錄
- [命令表](#命令表)
- [命令參數詳情](#命令參數詳情)

命令參數 `<>` 是必填項； `[]` 是選填項，且預設值會顯示為 `[數值=預設值]`。

## 命令表
| 命令 | 例子 | 描述 | 僅管理員 | 聊天 | RCON |
|------|------|------|----------|------|------|
| `/reloadcfg` | `/reloadcfg` | 重新載入 PalGuard 配置檔案。 | X | X | X |
| `/kick <玩家名稱>` | `/kick Cheater007` | 根據玩家名稱將其踢出伺服器。 | X | X | X |
| `/kickid <steamID>` | `/kickid 76567890987654321` | 根據玩家的 Steam ID 將其踢出伺服器。 | X | X | X |
| `/ban <玩家名稱>` | `/ban Cheater007` | 根據玩家名稱將其加入伺服器黑名單。 | X | X | X |
| `/banid <steamID>` | `/banid 76567890987654321` | 根據 Steam ID 將玩家加入伺服器黑名單。 | X | X | X |
| `/ipban <玩家名稱>` | `/ipban Cheater007` | 根據玩家名稱將該玩家的 IP 地址加入伺服器黑名單。 | X | X | X |
| `/ipbanid <steamID>` | `/ipbanid 76567890987654321` | 根據 Steam ID 將該 Steam ID 的 IP 地址加入伺服器黑名單。 | X | X | X |
| `/ipban_ip <IP>` | `/ipban_ip 127.0.0.1` | 將指定 IP 地址加入伺服器黑名單。 | X | X | X |
| `/unban_ip <IP>` | `/unban_ip 127.0.0.1` | 將指定 IP 地址移出伺服器黑名單。 | X | X | X |
| `/addadminip <IP>` | `/addadminip 127.0.0.1` | 將指定 IP 地址新增到管理員白名單。 | X | X | X |
| `/setadmin <steamID>` | `/setadmin 76567890987654321` | 臨時授予/撤銷玩家管理員許可權。 | X | X | X |
| `/renameplayer <steamID> <NewName>` | `/renameplayer 76567890987654321 Palworld God` | Renames a Player that is currently online. | X | X | X |
| `/getip <steamID>` | `/getip 76567890987654321` | 獲取玩家的 IP 地址。（玩家必須線上） | X | X | X |
| `/give <steamID> <物品ID> [數量=1]` | `/give 76567890987654321 LuxuryMedicines 42` | 給玩家一個物品，並可指定數量。 | X | X | X |
| `/giveitems <steamID> <物品ID>[:<數量>] ...` | `/giveitems 76567890987654321 LuxuryMedicines:42 Money:666 AssaultRifle_Default5` | 一次給玩家多個物品，並可以指定每個物品的數量，使用冒號分隔。 | X | X | X |
| `/giveme <物品ID> [數量=1]` | `/giveme Lotus_hp_02 999` | 給自己一個物品，並可指定數量。 | X | X | |
| `/delitem <steamID> <物品ID> [數量=1]` | `/delitem 76567890987654321 LuxuryMedicines all` | 從玩家身上刪除物品，並可指定數量，預設刪除一個物品。如果使用 `all`，將刪除所有該物品。 | X | X | X |
| `/delitems <steamID> <物品ID>[:<數量>] ...` | `/delitems 76567890987654321 LuxuryMedicines Milk:all Money:5000` | 一次刪除多個物品，並可指定每個物品的數量，通過冒號分隔。使用 `all` 替代 `1` 刪除所有該物品。 | X | X | X |
| `/give_exp <steamID> <數量>` | `/give_exp 76567890987654321 400000` | 給玩家指定數量的經驗值。 | X | X | X |
| `/giveme_exp <數量>` | `/giveme_exp 400000` | 給自己指定數量的經驗值。 | X | X | |
| `/whitelist_add <steamID>` | `/whitelist_add 76567890987654321` | 將 Steam ID 新增到白名單中。 | X | X | X |
| `/whitelist_remove <steamID>` | `/whitelist_remove 76567890987654321` | 從白名單中移除 Steam ID。 | X | X | X |
| `/whitelist_get` | `/whitelist_get` | 獲取所有已新增到白名單中的玩家列表。 | X | X | X |
| `/givepal <steamID> <PalId> [Level=1]` | `/givepal 76567890987654321 FengyunDeeper 55` | 給玩家一個帕魯（如果玩家攜帶的帕魯已滿，將進入帕魯終端）。All attributes are randomized. | X | X | X |
| `/givemepal <PalId> [Level=1]` | `/givemepal FengyunDeeper 55` | Gives yourself a Pal (if your party is full, it will go into your Pal storage). All attributes are randomized. | X | X | |
| [/givepal_j](givepal_j_ZH_CN.md) | `/givepal_j <steamID> <PalJSON>` | 給玩家一個帕魯，具有提供的 JSON 屬性。（如果玩家攜帶的帕魯已滿，將進入帕魯終端）。All attributes are randomized if not provided by the json file. 有關更多資訊，請詳見 [PalJSON](../Files/PalJSON_ZH_CN#json-file-template)。 | X | X | X |
| `/givemepal_j <PalJSON>` | `/givemepal_j OPnubis` | Gives yourself a Pal with the provided attributes in the json. (if your party is full, it will go into your Pal storage). All attributes are randomized if not provided by the json file. See [PalJSON](../Files/PalJSON.md#json-file-template) for a deeper understanding. | X | X | |
| [/deletepals](deletepals_ZH_CN.md) | `/deletepals <steamID> <PalFilter>` | 根據過濾器從玩家的帕魯隊伍和帕魯終端中刪除多個帕魯。過濾器可以通過命令參數配置。 | X | X | X |
| `/exportpals <steamID>` | `/exportpals 76567890987654321` | 導出玩家的所有帕魯到 `Pal/Binaries/Win64/palguard/pals/` 資料夾。有關更多資訊，請詳見 [PalJSON](../Files/PalJSON_ZH_CN#json-file-template)。 | X | X | X |
| `/jetragon` | `/jetragon` | 給你一個管理員級別的空渦龍（它超快...）。 | X | X | |
| `/catwaifu` | `/catwaifu` | 給你一個管理員級別的暗巫貓，增加你的角色屬性。 | X | X | |
| `/giveegg <steamID> <EggID>` | `/giveegg 76567890987654321 PalEgg_Electricity_03` | 給玩家一個蛋，其中包含一個完全隨機的帕魯。蛋的型別隻影響孵化時間，而不會影響其中的帕魯。 | X | X | X |
| `/goto <X> <Y> <Z>` | `/goto 133.7 666 42` | 傳送到指定位置。 | X | X | |
| `/pgbroadcast <Text>` | `/pgbroadcast Hello, Palworld!` | 向伺服器中的所有玩家發送訊息，訊息可以包含空格。 | X | X | X |
| `/iwantplayerlist` | `/iwantplayerlist` | 打開 `伺服器內可以檢視其他玩家列表` ，直到下次伺服器重啟。 | X | X | X |
| `/getrconcmds` | `/getrconcmds` | 返回一個命令列表，列出所有可通過 RCON 使用的命令及其所需參數數量。例如：`getrconcmds:1;giveegg:2;give:2;` | X | | X |
| `/getnearestbase [X] [Y] [Z]` | `/getnearestbase 133.7 666 42` | 告訴你最近的基地所屬的公會名稱。**如果是 RCON 使用，則必須提供座標。** | X | X | X |
| `/gotonearestbase [X] [Y] [Z]` | `/gotonearestbase 133.7 666 42`<br>`/gotonearestbase` | 傳送到最近的基地。 | X | X | |
| `/killnearestbase [X] [Y] [Z]` | `/killnearestbase 133.7 666 42`<br>`/killnearestbase` | 銷燬最近的基地。（使用時請小心）。**如果是 RCON 使用，則必須提供座標。** | X | X | X |
| `/adminlogout` | `/adminlogout` | 退出管理員模式。 | X | X | X |
| `/toggleserverpvp` | `/toggleserverpvp` | 打開或者關閉 `伺服器內PVP` 和 `玩家對玩家的傷害` ，直到下次伺服器重啟。 | X | X | X |
| `/give_relic <steamID> <數量>` | `/give_relic 76567890987654321 666` | 給玩家一個或多個翠葉鼠雕像。 | X | X | X |
| `/giveme_relic <Amount>` | `/giveme_relic 666`|Gives yourself one or more Lifmunk Effigies. | X | X | |
| `/givetech <platformID> [Count=1]` | `/givetech 76567890987654321 666`|Gives the player one or more Technology Points. | X | X | X |
| `/givemetech [Count=1]` | `/givemetech 666` | Gives yourself one or more Technology Points. | X | X | |
| `/givebosstech  <platformID> [Count=1]` | `/givebosstech 76567890987654321 666`|Gives the player one or more Ancient Technology Points. | X | X | X |
| `/givemebosstech [Count=1]` | `/givemebosstech 666`|Gives yourself one or more Ancient Technology Points. | X | X | |
| `/setguildleader <steamID>` | `/setguildleader 76567890987654321` | 讓目標玩家成為他目前公會的會長。 | X | X | X |
| `/imcheater` | `/imcheater` | 將你標記為作弊者並採取措施（用於測試反作弊）。 | X | X | X |

<br>

## 命令參數詳情
| 參數 | 描述 |
|------|------|
| 數量<br>等級 | 自然數（正整數）。 |
| X, Y, Z | 遊戲世界中的座標。 |
| [steamID](https://steamid.io) | Steam ID 是用來唯一標識 Steam 賬戶的識別符號。Steam ID 可以轉換為更新后的 steamID3 或 steamID64，也就是社區 ID 或好友 ID。通過該 steamID64，可以找到使用者的 Steam 社區頁面。 |
| 玩家名稱 | 玩家可以在遊戲過程中選擇和修改的最多 24 個字元的名稱。 |
| [IP](https://en.wikipedia.org/wiki/IP_address) | IP 地址（Internet Protocol 地址）是分配給連線到計算機網路（使用網際網路協議進行通訊）裝置的數字標籤，例如 192.0.2.1。IP 地址主要用於兩種功能：網路介面識別和位置定位。 |
| [物品ID](https://pwmodding.wiki/docs/game-data/item-table) | 用於標識物品的唯一名稱。 |
| [PalID](https://pwmodding.wiki/docs/game-data/monster-table) | 用於標識帕魯的唯一名稱。 |
| [EggID](https://pwmodding.wiki/docs/game-data/item-table) | 僅適用於蛋的物品 ID：<br>`PalEgg_Dark_01（暗黑帕魯蛋）` 到 `PalEgg_Dark_05（巨大暗黑帕魯蛋）`、`PalEgg_Dragon_01（龍蛋）` 到 `PalEgg_Dragon_05（巨大龍蛋）`、<br>`PalEgg_Earth_01（粗糙帕魯蛋）` 到 `PalEgg_Earth_05（巨大粗糙帕魯蛋）`、`PalEgg_Electricity_01（電氣帕魯蛋）` 到 `PalEgg_Electricity_05（巨大電氣帕魯蛋）`、<br>`PalEgg_Fire_01（發熱帕魯蛋）` 到 `PalEgg_Fire_05（巨大發熱帕魯蛋）`、`PalEgg_Ice_01（結冰帕魯蛋）` 到 `PalEgg_Ice_05（巨大結冰帕魯蛋）`、<br>`PalEgg_Leaf_01（新綠帕魯蛋）` 到 `PalEgg_Leaf_05（巨大新綠帕魯蛋）`、`PalEgg_Normal_01（平凡帕魯蛋）` 到 `PalEgg_Normal_05（巨大平凡帕魯蛋）`、<br>`PalEgg_Water_01（潮濕帕魯蛋）` 到 `PalEgg_Water_05（巨大潮濕帕魯蛋）`。 |
| [PalJSON](../Files/PalJSON_ZH_CN#json-file-template) | 包含帕魯屬性的 JSON 文字或檔案。模板和更多內容請詳見 [PalJSON](../Files/PalJSON_ZH_CN#template)。 |
