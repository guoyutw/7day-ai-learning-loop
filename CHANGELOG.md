# CHANGELOG

## 2026-11-12 — v0.2 / Research-first rewrite (public candidate)

**為何改**：最初 v0.1 把使用者原來的跨語言／跨平台研究方法縮成「直接產生七天課表」，遺失完整長影片、社群原始材料、NotebookLM 來源匯入驗收、跨來源證據分級與研究停止關卡。

**這次修改**：
- 重寫 README：研究先於課程，清楚展示 R0–R4 流程與兩個確認關卡。
- 重寫 PROMPT：先界定問題、搜尋／驗收完整來源、跨來源比對與反例，SOURCE_REVIEW 後才設計七天，PLAN_REVIEW 後才開始 Day 1。
- 新增 RESEARCH_METHOD、SOURCE_LOG_TEMPLATE：來源搜尋、影片視覺缺失、FULL/PARTIAL、AI 二次報告、去重、來源可靠性及停止條件。
- 新增 RESEARCH_PROMPTS：不同研究工具（一般搜尋 AI／Grok X／Meta AI Threads／Gemini Notebook）之精確分工與手動交接。
- 新增 ORIGIN：公開描述方法形成的研究脈絡，不公開私人案例或原始紀錄。
- 修正 METHOD、DAILY_REVIEW、HANDOFF：以來源支持的實作、原始基線、批改重做、轉移與跨對話接續為主。
- SOURCES 改列各來源的作用與證據限制，避免把公開網址當作方法效能的證明。

**仍然未知**：尚未完整跑過七天、沒有學習效果比較、沒有跨模型穩定性或成本測量；v0.2 的正確性僅代表文件構造與來源邊界已明示，**不代表實際教學已通過驗證**。

## 2026-11-12 — v0.1 / Initial public release

第一版僅包含基本七天規劃、每日練習與回顧及跨對話模板；後續發現缺乏原本以研究來源為中心的完整工作流程，因此以 v0.2 修正。
