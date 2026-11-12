# 中斷接續｜一份狀態就夠

每次結束研究階段或一天的練習，請 AI 依下表**只填實際已完成**的資訊，存到自己的筆記。新對話先貼 [PROMPT.md](PROMPT.md) 的完整提示詞，**再貼這份狀態**；不要重頭搜尋，也不要假稱讀到其他對話。

```text
【七天學習交接】
主題／七天作品：
目前程度、每日時間、重要限制：
研究問題與搜尋範圍（已完成的用原始結果／位置）：
目前階段：SOURCE_PACKAGE_READY／INGEST_REVIEW／等待 SYNTHESIS_REPORT／SOURCE_REVIEW／PLAN_REVIEW／Day __
模式：STANDARD／QUICK_MODE
路線：NOTEBOOKLM_FIRST／DIRECT_SYNTHESIS（若改用，附本人明確選擇）
來源清單：Sxx + URL 或私人文件位置；讀取缺口與 UNKNOWN：
NotebookLM 匯入紀錄：已成功／失敗／未知，以及收據位置（無則 PENDING）：
跨來源研究報告位置（無則 PENDING）：
SOURCE_REVIEW 本人確認：YES／NO／PENDING
SOURCE_REVIEW 核准的 1–3 個方法（或原始審查全文位置、來源 ID）：
七天計畫版本／全文位置（已產出就填，未產出為 PENDING）：
PLAN_REVIEW 本人確認：YES／NO／PENDING
已用 NEED_SOURCES 補搜輪次：0／1／2
目前 Day（尚未開始寫 NOT STARTED）：
本人原始作品／Day 1 基線位置：
今天實際做了什麼、AI 幫了什麼、本人重做了什麼：
實際結果、成本、反例及未證明事項：
唯一下一步：
```

**接續檢查**：比對已保存的研究問題、來源／收據、已確認方法、**原七天計畫全文或可讀位置**、學習者批准與當前階段。已有計畫且 PLAN_REVIEW=PENDING 時，先讀回既有版本交本人確認，**不得重寫課表**；缺原稿先請本人補既有原稿／位置，不能拿 AI 猜測取代。沒有收據或批准就保持 PENDING，不因 AI 生成的摘要自動補齊。切換 AI 時先做「唯一下一步」，除非目標更改或證據過期，不重跑已驗證工作。

每日回顧最少記錄**本人第一次做的版本、AI 回饋、本人重做版、下一步**；Day 7 再對照 Day 1 的相近任務。請把資料放私人空間，避免把客戶訊息、個人敏感內容或整份第三方付費教材貼到公開 Issue。
