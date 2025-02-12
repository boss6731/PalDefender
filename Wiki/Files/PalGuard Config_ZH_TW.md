### [<<<](README_ZH_TW.md) 檔案型別

#### [English](./PalGuard%20Config.md) / 繁體中文

# PalGuard.json

以下是每個配置項的的說明:
| 配置項 | 值 | 說明 |
|--------|-----|------|
| `RCONbase64` | true, false | 設定為`true`可以在RCON中使用Base64編碼 優點：適用於unicode字元（中文/韓語/俄語/等）缺點： 您只能使用支援編碼/解碼 base64的RCON客戶端。 |
| `adminAutoLogin` | true, false | 如果您的IP與管理員白名單匹配，則自動授予您管理員許可權。 |
| `adminIPs` | `["127.0.0.1", "..."]` | 允許使用管理員指令的白名單IP地址列表。 |
| `allowAdminCheats` | true, false | 允許管理員進行作弊行為而不會受到懲罰。 |
| `announceConnections` | true, false | 當玩家加入/離開伺服器時廣播訊息。 |
| `announcePunishments` | true, false | 當玩家被反作弊系統踢出或封禁時廣播訊息。 |
| `bannedChatWords` | `["word1", "word2", "..."]` | 用於過濾RMT（即現實金錢交易，用現實貨幣交易虛擬物品的行為）廣告的單詞列表。包含這些詞的訊息將被阻止。 |
| `bannedIPs` | `["127.0.0.1", "..."]` | 被封禁的IP地址列表。 |
| `bannedMessage` | "You are banned." | 允許您自定義玩家在 IP 被禁止時嘗試加入您的伺服器時看到的訊息（支援中文）。 |
| `bannedNames` | `["anquan666", "Goldberg"]` | 一些基本的盜版保護（封禁的玩家昵稱）。 |
| `blockTowerBossCapture` | true, false | 啟用/禁用捕捉高塔boss。 |
| `chatBypassWait` | true, false | 可以讓你在發送聊天資訊時不再有1分鐘的冷卻時間。 |
| `disableButchering` | true, false | 禁用屠宰功能，以防止無限屠宰的物品複製漏洞。 |
| `disableIllegalItemProtection` | true, false | 禁用對除錯/搶劫球體（某些模組將其作為可製作物品新增到遊戲中）的保護。 |
| `disablePalRenaming` | true, false | Disables Pal renamings. |
| `disableRenaming` | true, false | 禁用玩家重新命名功能（他們仍然可以改寵物的名字）。 |
| `doActionUponIllegalPalStats` | true, false | 檢測到作弊時執行操作（設定為 false，則在檢測到作弊時不會執行踢出或封禁等操作，需要人工判斷）。 |
| `isChineseCmd` | true, false | 如果你希望顯示中文字元並使用預設的windows命令列，請將此設定為`true`。在較新的Windows版本中可以忽略。 |
| `logChat` | true, false | 將所有聊天訊息記錄到日誌。 |
| `logNetworking` | true, false | 將玩家發送給伺服器的幾乎所有網路數據記錄到日誌。 |
| `logPlayerIP` | true, false | Additionally logs the player IP whenever a log contains a player. |
| `logPlayerUID` | true, false | Additionally logs the player UniqueID whenever a log contains a player. |
| `logRCON` | true, false | 將所有RCON命令記錄到日誌。 |
| `palStatsMaxRank` | 任何正數（包括0） | 設定強化帕魯的最大等級限制。設定為0任何玩家都無法強化帕魯。任何大於0的數值將設定新的限制，預設為10。如果設定為-1，將檢測伺服器的最大帕魯強化等級，並相應地更新此值。 |
| `pveMaxToPalBanThreshold` | 任何正數 | 嘗試對高於此數值的帕魯造成傷害時，將標記為作弊者。 |
| `pvpMaxToPalDamage` | 任何正數 | 如果啟用PVP（bEnablePlayerToPlayerDamage），玩家對帕魯造成的最大傷害超過此數值，將會被限制為該數值。此選項適用於未經任何傷害減免的傷害。 |
| `pvpMaxToBuildingDamage` | 任何正數 | 同`pvpMaxToPalDamage`，但針對建築物。此選項適用於未經任何傷害減免的傷害。 |
| `shouldBanCheaters` | true, false | 允許反作弊系統自動封禁作弊者。 |
| `shouldIPBanCheaters` | true, false | 允許反作弊系統自動封禁作弊者IP。 |
| `shouldKickCheaters` | true, false | 允許反作弊系統自動踢出作弊者。 |
| `shouldWarnCheaters` | true, false | 允許反作弊系統在聊天中警告作弊者。 |
| `shouldWarnCheatersReason` | true, false | 提供作弊者被警告的原因。 |
| `steamidProtection` | true, false | 防止相同的SteamID在玩家已經登錄時再次加入伺服器。 |
| `useAdminWhitelist` | true, false | 啟用/禁用管理員IP白名單系統（僅有adminIPs中的IP地址的玩家可以通過/adminpassword指令獲得管理員許可權）。 |
| `useWhitelist` | true, false | 啟用/禁用SteamID白名單（僅有在SteamID白名單列表中的玩家可以進入伺服器）。 |
| `whitelistMessage` | "You are not whitelisted." | 自定義未被列入白名單時顯示的訊息（支援中文）。 |
