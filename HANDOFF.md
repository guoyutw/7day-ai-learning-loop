# 中斷接續｜一份狀態就夠

每次結束研究階段或一天的練習，請 AI 依下表**只填實際已完成**的資訊，存到自己的筆記。新對話先貼 [PROMPT.md](PROMPT.md) 的完整提示詞，**再貼這份狀態**；不要重頭搜尋，也不要假稱讀到其他對話。

```text
【七天學習交接】
主題／七天作品：
目前程度、每日時間、重要限制：
目前階段：SOURCE_PACKAGE_READY／INGEST_REVIEW／等待 SYNTHESIS_REPORT／SOURCE_REVIEW／PLAN_REVIEW／Day __
模式：STANDARD／QUICK_MODE
路線：NOTEBOOKLM_FIRST／DIRECT_SYNTHESIS（若改用，附本人明確選擇）
來源清單：Sxx + URL 或私人文件位置；讀取缺口與 UNKNOWN：
NotebookLM 匯入紀錄：已成功／失敗／未知，以及收據位置（無則 PENDING）：
跨來源研究報告位置（無則 PENDING）：
SOURCE_REVIEW 本人確認：YES／NO／PENDING
PLAN_REVIEW 本人確認：YES／NO／PENDING
已用 NEED_SOURCES 補搜輪次：0／1／2
目前 Day（尚未開始寫 NOT STARTED）：
本人原始作品／Day 1 基線位置：
今天實際做了什麼、AI 幫了什麼、本人重做了什麼：
實際結果、成本、反例及未證明事項：
唯一下一步：
```

**接續檢查**：比對已保存的收據、學習者批准與當前階段；只有必要證據完整才前進。沒有收據或批准就保持 PENDING，不因 AI 生成的摘要自動補齊。若只是切換 AI，先從「唯一下一步」接續，除非使用者更換目標或來源證據已過期，不重跑已驗證工作。

每日回顧最少記錄**本人第一次做的版本、AI 回饋、本人重做版、下一步**；Day 7 再對照 Day 1 的相近任務。請把資料放私人空間，避免把客戶訊息、個人敏感內容或整份第三方付費教材貼到公開 Issue。
