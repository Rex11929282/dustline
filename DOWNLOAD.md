# Dustline 下載入口

這是 **Rex11929282** 的打包與下載入口副本。原 Windows 遊戲來自 [mmsx4717/dustline](https://github.com/mmsx4717/dustline)，原作者與素材權利歸各自權利人所有；本副本沒有將原遊戲改稱為 Rex 自行開發。

## 網站與下載

- [開啟 Dustline Play Hub](https://dustline-play-hub-5zczhy.v2.appdeploy.ai/)
- [完整 Windows 下載包 / GitHub Releases](https://github.com/Rex11929282/dustline/releases)
- [查看完整包的打包、校驗與發布紀錄](https://github.com/Rex11929282/dustline/actions/workflows/publish-windows-zip.yml)
- [獨立網頁試玩](https://dustline-play-hub-5zczhy.v2.appdeploy.ai/play.html)

請下載 Release 附件 **`Dustline-Windows-x64.zip`**，不要把 GitHub 的 `Source code (zip)` 當作完整遊戲。完整包只有在 Git LFS 資源取得、全部 165 項 SHA256 校驗以及壓縮後讀回校驗通過後，才會正式發布。Release 沒有該附件時，代表完整包還不能下載；網站會保留備援下載器。

## Windows 開啟方式

1. 下載完整 ZIP，右鍵選「解壓縮全部」。不要在 ZIP 裡直接執行。
2. 打開解壓後的 `Dustline` 資料夾，執行 `Install-Dustline.cmd`，輸入 `Y` 確認。
3. 等待 `SUCCESS`，再從桌面或開始功能表的 `Dustline` 捷徑開啟。

離線安裝預設位置為 `%LOCALAPPDATA%\Programs\Dustline`。完整包已含遊戲，不需要再從 Git LFS 下載；安裝程式只校驗、複製本機檔案並建立捷徑，不會自動啟動遊戲。也可直接從完整解壓後的資料夾執行 `Start-Dustline.cmd`。

請讓 `Dustline.exe`、`UnityPlayer.dll`、`Dustline_Data`、`MonoBleedingEdge`、`D3D12` 等檔案留在同一套遊戲目錄，不要單獨搬動 EXE。既有備援下載器的部分下載不能直接當成完整 ZIP；不要刪除舊檔來嘗試加速。

## 版本與校驗

固定遊戲版本為 `0.6.6 build24-public`，來源提交為 `330d14e68b7716ec49c791152398d3f8e4d2b131`。Release 提供整包的 `.sha256` 與 `package-info.json`，其中記錄實際 ZIP 大小、原遊戲檔案大小及校驗結果。完整包的遊戲位元組維持原樣；ZIP 壓縮不等於解壓後的遊戲素材已縮減。

此流程不會執行遊戲 EXE，文件完整性校驗也不代表已完成 Windows 遊玩、聯機相容性或安全性實測。Windows 版自動區網找房與 Unity 原版移植至瀏覽器仍未完成。網站的網頁試玩是獨立製作的輕量單人版本。

## 重新打包

本倉庫的 `Publish Dustline Windows ZIP` 支援手動 `Run workflow`。流程只會對 `Rex11929282/dustline` 發布，不修改原作者倉庫。若相同 Release tag 已存在，流程會拒絕覆蓋既有下載附件；請先決定新版本／新標籤再發布，不要任意覆蓋玩家正在下載的包。
