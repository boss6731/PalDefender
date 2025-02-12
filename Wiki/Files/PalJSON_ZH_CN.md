### [<<<](README_ZH_CN.md) 檔案型別

#### [English](./PalJSON.md) / 繁體中文

# PalJSON

### 目錄
- [描述](PalJSON_ZH_TW.md#描述)
- [屬性](PalJSON_ZH_TW.md#屬性)
- [模板](PalJSON_ZH_TW.md#模板)
- [預設](PalJSON_ZH_TW.md#預設)

## 描述
PalJSON 是一個 JSON 檔案，用於定義正在建立的帕魯的屬性。**它必須包含 `CharacterID`，否則建立過程會失敗。**

檢視預設值：[GitHub/iiLarsH/Chillet/csv's/PalData.csv](https://github.com/iiLarsH/Chillet/blob/698b5ea1190177533dc7924f9af9e40ff8ee4776/csv's/PalData.csv)

## 屬性

| 參數 | 值型別 | 值（示例） | 描述 |
|----|--------|------------|------|
| `CharacterID` | 字串，包含 [PalID](https://pwmodding.wiki/docs/game-data/monster-table) | "..." | 確定該帕魯是哪個。 |
| `NickName` | 字串 | "..." |帕魯的顯示名稱。 |
| `UniqueNPCID` | 字串 | "..." |  |
| `Gender` | 整數 | 1 = 男性<br>2 = 女性 |  |
| `Level` | 整數 | 0 - 255 |帕魯的等級。 |
| `Exp` | 整數 | 0 到 2^63 |帕魯擁有的經驗值。 |
| `IsRarePal` | 布爾值 | true 或 false | 是否為稀有帕魯。 |
| `MaxHP` | 整數 | 0 到 2^63 |帕魯的最大血量。 |
| `Hp` | 整數 | 0 到 2^63 |帕魯目前的血量。 |
| `MaxMP` | 整數 | 0 到 2^63 |帕魯的最大 MP。 |
| `MP` | 整數 | 0 到 2^63 |帕魯目前的 MP。 |
| `MaxSP` | 整數 | 0 到 2^63 |帕魯的最大體力值。 |
| `ShieldMaxHP` | 整數 | 0 到 2^63 |帕魯的最大盾牌血量。 |
| `ShieldHP` | 整數 | 0 到 2^63 |帕魯目前的盾牌血量。 |
| `FullStomach` | 浮動數 | 0.0 到 ?? |帕魯目前的飽腹度。 |
| `MaxFullStomach` | 浮動數 | 0.0 到 ?? |帕魯的最大飽腹度。最高的預設值在帕魯中為 `600.0`。 |
| `Support` | 整數 | 0 到 2^31 |  |
| `CraftSpeed` | 整數 | 0 到 2^31 |帕魯的基礎工作速度，預設值為 `100`。 |
| `SanityValue` | 浮動數 | 0.0 到 ?? |帕魯目前的 SAN（理智值）。 |
| `UnusedStatusPoint` | 整數 | 0 到 2^16 |  |
| `Rank` | 整數 | 0 - 255 |  |
| `RankUpExp` | 整數 | 0 - 255 |  |
| `Rank_HP` | 整數 | 0 - 255 |  |
| `Rank_Attack` | 整數 | 0 - 255 |  |
| `Rank_Defence` | 整數 | 0 - 255 |  |
| `Rank_CraftSpeed` | 整數 | 0 - 255 |  |
| `Talent_HP` | 整數 | 0 - 255 |  |
| `Talent_Melee` | 整數 | 0 - 255 |  |
| `Talent_Shot` | 整數 | 0 - 255 |  |
| `Talent_Defense` | 整數 | 0 - 255 |  |
| `EquipWaza` | 字串陣列，包含 [EPalWazaIDs](../Data%20Lists/EPalWazaIDs_ZH_TW.md) | ["", "", ""] |帕魯目前裝備的技能。 |
| `MasteredWaza` | 字串陣列，包含 [EPalWazaIDs](../Data%20Lists/EPalWazaIDs_ZH_TW.md) | ["", "", "", ""] |帕魯已學會的技能。 |
| `PassiveSkillList` | 字串陣列，包含 [PassiveSkills](../Data%20Lists/PassiveSkills_ZH_TW.md) | ["", "", "", ""] |帕魯擁有的所有被動技能。 |

## 模板
檔案必須放置在 [`Pal/Binaries/Win64/palguard/pals/`](../../README_ZH_TW.md#windows)
```json
{
    "NickName": "",
    "CharacterID": "",
    "UniqueNPCID": "",
    "Gender": 1,
    "Level": 1,
    "Exp": 0,
    "IsRarePal": false,
    "MaxHP": 100,
    "Hp": 100,
    "MaxMP": 100,
    "MP": 100,
    "MaxSP": 100,
    "ShieldMaxHP": 0,
    "ShieldHP": 0,
    "FullStomach": 600.0,
    "MaxFullStomach": 600.0,
    "Support": 100,
    "CraftSpeed": 100,
    "SanityValue": 100.0,
    "UnusedStatusPoint": 0,
    "Rank": 0,
    "RankUpExp": 0,
    "Rank_HP": 0,
    "Rank_Attack": 0,
    "Rank_Defence": 0,
    "Rank_CraftSpeed": 0,
    "Talent_HP": 0,
    "Talent_Melee": 0,
    "Talent_Shot": 0,
    "Talent_Defense": 0,
    "EquipWaza": [],
    "MasteredWaza": [],
    "PassiveSkillList": []
}
```

## 預設
* [OPnubis](PalJSON%20Presets/OPnubis.json) - Anubis，所有屬性已最大化。
