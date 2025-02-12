### [<<<](README_ZH_TW.md) 命令

#### [English](./deletepals.md) / 繁體中文

# /deletepals

| |許可權|
|-|:---------:|
|僅管理員|X|
|聊天|X|
|RCON|X|

### 描述
根據過濾器從玩家的帕魯隊伍和帕魯終端中刪除多個帕魯。過濾器可以通過命令參數配置。被刪除的帕魯將建立一個 .json 檔案，以便在使用不當時恢復帕魯。目前需要手動查詢檔案，未來版本計劃提供一個恢復帕魯的命令。

被刪除的帕魯可以在 `<palserver_root>/Pal/Binaries/Win64/palguard/pals/deleted/<SteamID>/` 中找到。

### 語法

```cmd
/deletepals <steamID> <PalFilter>
```

### PalFilter
該過濾器允許在一個命令列中使用多個關鍵字來刪除符合條件的帕魯。第一次使用時可能會比較複雜，所以請先在測試環境中嘗試。

以下是過濾器關鍵字及其說明：
|關鍵字|值|符號|說明|
|-|:---------:|:---------:|-|
|ID|[PalID](../Data%20Lists/Pals.md) 或帕魯列表|無|一個或多個 ID，使用 `,` 逗號分隔。不要用來忽略 ID 的過濾。|
|Nick|字串|無|過濾帕魯的名稱。如果不需要，請不要使用。|
|Gender|`male` 或 `female`|無|按性別過濾。如果不需要過濾性別，請不要使用。|
|Level|數字|`<`, `>`, `<=`, `>=`, `=`, `!=`|按等級過濾。使用符號指定。例如，`Level>=35` 會包括等級為 35 及以上的帕魯。|
|Rank|數字|`<`, `>`, `<=`, `>=`, `=`, `!=`|按排名過濾。使用符號指定。例如，`Rank>1` 會包括排名高於 1 的帕魯。排名是根據相同帕魯的綜合排名。|
|Lucky|`true` 或 `false`|無|過濾是否為稀有（閃亮）夥伴。|
|Passives|[PassiveSkill](../Data%20Lists/PassiveSkills_ZH_TW.md) 或被動技能列表|無|一個或多個 ID，使用 `,` 逗號分隔。不要用來忽略技能的過濾。|
|Limit|數字|無|限制過濾結果的數量。例如，`Limit 5` 會使過濾器只找到 5 個帕魯，即使可以找到更多。|

### 用法  
```cmd
/deletepals 76567890987654321 ID Serpent, PinkLizard Level>10 Gender male Limit 3
```
這將刪除最多 3 個等級高於 10 的帕魯（因此等級為 10 或以下的帕魯不會被刪除），性別為男性，且帕魯為滑水蛇或博愛蜥。
<br>
<br>
<br>

```cmd
/deletepals 76567890987654321 ID Anubis Rank >= 3
```
這將刪除所有排名為 3 或以上的阿努比斯。
<br>
<br>
<br>

```cmd
/deletepals 76561198033277828 Passives CraftSpeed_up1,CraftSpeed_up2,Rare,PAL_CorporateSlave
```
這將刪除擁有所有 4 個被動技能的帕魯。

被動技能如下：
- CraftSpeed_up1 = Serious（認真）<br>
- CraftSpeed_up2 = Artisan（工匠精神）<br>
- Rare = Lucky（稀有）<br>
- PAL_CorporateSlave = Work Slave（社畜）<br>

因此，需要擁有這 4 個被動技能，如果只擁有 3 個，它將被忽略。
