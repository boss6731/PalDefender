# PalGuard v1.1273 (幻獸帕魯伺服器反作弊)

#### [English](/README.md) / 繁體中文

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/T6T014OZZB)


[![Discord Server](https://img.shields.io/badge/-Discord-111111?style=for-the-badge&logo=discord)](https://discord.com/invite/bdTxPbwSEW)
[![Static Badge](https://img.shields.io/badge/-Nexus%20Mods-111111?style=for-the-badge&logo=nexusmods)](https://www.nexusmods.com/palworld/mods/451)


## 目錄
* [關於](#關於-)
* [需求](#需求-)
* [安裝](#安裝-)
   - [Windows](#windows)
   - [Linux (Wine/Proton)](#linux-wineproton)
* [功能](#功能-)
* [Wiki](#wiki-)
* [作者](#作者-)
* [致謝](#致謝-)
* [後記](#後記-)

## 關於 [↑](#palguard-v11066-幻獸帕魯伺服器反作弊)

實現了全面的服務端驗證，防止已知和一些尚未發現的作弊、漏洞和崩潰。PalGuard 在執行任何玩家操作之前會檢查潛在的作弊行為。根據伺服器的配置，嘗試這些操作的玩家會被警告、踢出、封禁或 IP 封禁。目前，這一功能處於測試階段，僅在基於 Windows 的伺服器上可用。**任何有經驗的 Linux 開發者都歡迎來幫助我們。**

程式碼是閉源的，我們沒有計劃發佈它。

<br>

## 需求 [↑](#palguard-v11066-幻獸帕魯伺服器反作弊)

- [Microsoft Visual C++ 最新版本的可再發行元件](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)
  我不確定在 Proton 或 Wine 上如何使用，但根據反饋，它似乎可以開箱即用。

<br>

## 安裝 [↑](#palguard-v11066-幻獸帕魯伺服器反作弊)

### Windows

1. 在 [NexusMods.com](https://www.nexusmods.com/palworld/mods/451) 下載最新版本
2. 解壓內容並將其放入你的 PalServer 子目錄 `Pal\Binaries\Win64`
   目錄結構應如下所示：
   ```
   Palworld_Server/
   ├── Engine/
   ├── Pal/
   │   ├── Binaries/
   │   │   └── Win64
   │   │       ├── config/
   │   │       ├── palguard/                         # 將產生此資料夾
   │   │       ├── <...>
   │   │       ├── PalGuard.dll                      # << 放在此處
   │   │       ├── version.dll                       # << 放在此處
   │   │       ├── PalServer-Win64-Shipping-Cmd.exe
   │   │       └── PalServer-Win64-Shipping.exe
   │   ├── Content/
   │   ├── Plugins/
   │   └── Saved/
   ├── PalServer.exe
   ├── steamclient.dll
   └── <...>
   ```
3. 啟動伺服器一次以產生配置檔案 `PalGuard.json`，該檔案會產生在 PalGuard.dll 同目錄下。

### Linux (Wine/Proton)

1. 安裝 Palworld Proton/Wine 伺服器（此部分不在本文涵蓋範圍內）。
2. 在伺服器上安裝 [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS)。
3. 按照 Windows 安裝步驟操作。

## 功能 [↑](#palguard-v11066-幻獸帕魯伺服器反作弊)

* 作弊和漏洞檢測、預防與懲罰
* 更多的管理員命令（包括 RCON）
* IP 封禁系統
* 管理員命令的 IP 白名單（防止作弊者使用管理員命令）
* 聊天記錄
* RCON REST網路日誌
* 可配置的作弊懲罰
* PvP 傷害限制（儘管我們建議完全禁用 PvP）
* 一些遊戲機制調整，如限制帕魯強化或禁用肢解

<br>

## Wiki [↑](#palguard-v11066-幻獸帕魯伺服器反作弊)

關於 PalGuard 和它的使用，詳細資訊可以檢視 [Wiki](Wiki/README_ZH_CN.md)。

<br>

## 作者 [↑](#palguard-v11066-幻獸帕魯伺服器反作弊)

- [Ultimeit](https://github.com/Ultimeit)
- [Zvendson](https://github.com/Zvendson)

<br>

## 致謝 [↑](#palguard-v11066-幻獸帕魯伺服器反作弊)

* [Pocketpair, Inc.](https://www.pocketpair.jp/palworld)
* [Unreal Engine](https://www.unrealengine.com) - Epic Games

<br>

## 後記 [↑](#palguard-v11066-幻獸帕魯伺服器反作弊)

**私たちは、[Pocketpair, Inc.](https://www.pocketpair.jp/palworld)による素晴らしい仕事に感謝の意を表したいと思います。色鮮やかな世界や、パルとのダイナミックなインタラクション、そして創造的なデザインは、チームの獻身と情熱を見事に表しています。コミュニティの一員として、私たちはPalServer向けのプラグインを開発し、セキュリティを強化し、潛在的な悪用から守ることでPalworldをサポートしています**

**私たちは今後も、Palworldサーバーに最高水準のセキュリティと保護を提供できるよう努め続けます。皆様からのフィードバックは非常に貴重で、心から感謝しています。**<br>
~ [Zvend](https://github.com/Zvendson)

> *我們想向 [Pocketpair, Inc.](https://www.pocketpair.jp/palworld) 表達我們的感謝，感謝他們為幻獸帕魯所做的非凡工作。色彩斑斕的世界、與帕魯的動態互動以及創意設計都展示了團隊的奉獻精神和熱情。作為社區的一員，我們也在為幻獸帕魯開發服務端外掛，增強安全性，並保護其免受潛在的漏洞攻擊。*
<br><br>
*我們將繼續努力，為您的幻獸帕魯伺服器提供最高水平的安全性和保護。您的反饋至關重要，我們由衷地感謝。*
