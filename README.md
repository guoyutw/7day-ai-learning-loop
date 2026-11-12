# 用免費教材，做一套自己的 7 天 AI 學習課

網路上有完整的公開課、YouTube 長影片和專家文章，只是散落在不同語言與平台。這套方法讓 AI 先找資料、交給 NotebookLM 比較，再陪你練七天。

**[開始：複製啟動提示詞 →](PROMPT.md)**

填入想學的主題、目前程度和每天可用時間，將完整提示詞貼到有搜尋能力的 AI。**不用寫程式，也不用先讀其他文件。**

<details>
<summary>第一次使用，接下來會發生什麼？</summary>

1. AI 先提供帶原始網址的教材清單和 NotebookLM 匯入指示，**停下來等你**。
2. 你將選好的免費來源匯入 [NotebookLM](https://notebooklm.google.com/)，把匯入結果帶回原 AI；它再給你跨來源比較指示。
3. 你把 NotebookLM 的整理結果帶回 AI，確認研究方向和七天計畫之後，才開始 Day 1。

這是**跨工具、部分需要手動複製**的流程，不是全自動服務。研究花的時間不算在七天練習內。沒有 NotebookLM 時，可要求 AI 提供替代路線，**由你決定是否改用**。

</details>

<details>
<summary>中斷了、AI 跳步了，怎麼辦？</summary>

- **AI 直接排課**：請它回到 `SOURCE_PACKAGE_READY`，先交教材來源與 NotebookLM 匯入指示。
- **換 AI／換對話**：先貼 [PROMPT.md](PROMPT.md) 的完整指令，再貼上依 [HANDOFF.md](HANDOFF.md) 保存的最新狀態，從尚未完成的步驟繼續。
- **NotebookLM 匯入失敗**：告訴原 AI 哪些來源失敗；不代表原文章一定無法讀取。
- **時間不足**：可明確要求 `QUICK_MODE`（最多 3 個來源）；其他確認步驟不會省略。

</details>

<details>
<summary>方法細節與公開紀錄</summary>

- [PROMPT.md](PROMPT.md)：唯一完整 AI 啟動指令，含停止與人工確認關卡。
- [METHOD.md](METHOD.md)：研究證據、NotebookLM 接力、七天練習與驗收（按需閱讀）。
- [HANDOFF.md](HANDOFF.md)：跨對話接續與每日紀錄（按需使用）。
- [ORIGIN.md](ORIGIN.md)、[SOURCES.md](SOURCES.md)：方法起源與公開參考資料。
- [CHANGELOG.md](CHANGELOG.md)、[LICENSE](LICENSE)：改版紀錄與授權。

</details>

**公開試用，尚未驗證七天學習成效。** 免費教材不等於內容都正確；AI 讀到文章不等於方法有效，也不代表七天能學會。請勿上傳私人資料或未經授權的第三方教材。醫療、法律、財務與危險操作不以這套練習取代專業判斷。

試用遇到障礙，可在 [GitHub Issues](https://github.com/guoyutw/7day-ai-learning-loop/issues) 留下主題、使用的 AI 與卡住的步驟；不需要公開自己的對話或筆記。
