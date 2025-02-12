# PalGuard Wiki

#### [English](./README.md) / 繁體中文

## 目錄

- [命令](./Commands/README_ZH_TW.md)
- [檔案型別](./Files/README_ZH_TW.md)
- [數據列表](./Data%20Lists/README_ZH_TW.md)
- [常見問題解答](#faq)
  - [我不小心封禁了自己/別人。如何解除封禁？](#我不小心封禁了自己別人如何解除封禁)
  - [我無法以管理員身份登錄，顯示管理員命令被白名單保護。](#我無法以管理員身份登錄顯示管理員命令被白名單保護)
  - [我的伺服器在啟動時崩潰。](#我的伺服器在啟動時崩潰)
  - [我在伺服器控制檯中無法正確看到某些符號。](#我在伺服器控制檯中無法正確看到某些符號)
  - [如何報告崩潰？](#如何報告崩潰)

</details>

## 前言
此Wiki正在建設中，因此內容不完整。如果您能提供貢獻或指出錯誤，將有助於Wiki逐步完善。

## 常見問題解答
### 我不小心封禁了自己/別人。如何解除封禁？
如果是封禁了他們的IP，您需要暫時編輯`palguard.json`檔案，並重新載入配置或重啟伺服器。如果是封禁了他們的賬戶，您需要從`Pal\Saved\SaveGames\banlist.txt`中刪除他們的SteamID，並等待幾分鐘或在此之後重啟伺服器。

---

### 我無法以管理員身份登錄，顯示管理員命令被白名單保護。
確保您已將您的IP地址新增到`palguard.json`檔案中，如圖所示。或者，您可以將`useAdminWhitelist`設定為`false`，但這不推薦，因為已知作弊者有某種漏洞能夠獲取管理員密碼。

![AdminWhitelist](/.github/images/AdminWhitelist.png)

---

### 我的伺服器在啟動時崩潰。
請確保`palguard.json`檔案沒有配置錯誤，嘗試刪除該檔案並重新啟動伺服器。如果仍然無法解決問題，且這是您第一次使用PalGuard，建議安裝[VC++ redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)。

---

### 我在伺服器控制檯中無法正確看到某些符號。
請使用Windows Terminal（或任何支援Unicode的替代終端）代替預設的Windows控制檯。

---

### 如何報告崩潰？
Send your `\Pal\Saved\Crashes\*random numbers*\CrashContext.runtime-xml` file + palguard version used + log from `Pal\Binaries\Win64\logs` folder in [Bug Report Issues](https://github.com/Ultimeit/palguard/issues/new?template=BUG-REPORT.yml).

---
