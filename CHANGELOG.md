# CHANGELOG

## Unreleased — Draft：單一入口、按需載入、三條路徑走查

### Draft PR #1 針對審查反例的小修

- 重新補足 QUICK_MODE 必須明確選擇、最多 3 來源、標記證據信心較低，**仍走 NotebookLM-first**；DIRECT_SYNTHESIS 需另外明確選擇。
- HANDOFF 保存研究問題、已核准 1–3 個方法、七天計畫版本／全文定位；PROMPT 要求每次停止時輸出可貼回的接續狀態。PLAN_REVIEW=PENDING 且已存在課表時，**讀回原稿而不是重做**。
- 補回會影響行為的界線：只有搜尋摘要不能標 FULL、匯入成功不等於原文完整、NotebookLM 引用應能對回原 URL／章節、Grok／Meta AI 有界檢索、曝光／詢問／付款等不同事件不得互相推論。
- 維持單一主 Prompt 與四份文件整併；不恢復已刪文件，不代表通過獨立審查或真人端到端測試。


- **目的**：讓第一次進來的人迅速知道「免費教材 → NotebookLM 統整 → 七天實作」，單一主動作是開啟 `PROMPT.md`。
- **去重**：保留 `README.md`（給人）、`PROMPT.md`（唯一 AI 執行指令）、`METHOD.md`（研究及教學細節）、`HANDOFF.md`（跨對話狀態）；移除重複的 `RESEARCH_METHOD.md`、`RESEARCH_PROMPTS.md`、`SOURCE_LOG_TEMPLATE.md`、`DAILY_REVIEW.md`。研究背景、公開來源、版本紀錄與授權保留。
- **行為不變**：保留 STANDARD／QUICK_MODE、NotebookLM-first／需明確選擇的 DIRECT_SYNTHESIS、來源級別與畫面限制、SOURCE_PACKAGE_READY／INGEST_REVIEW／SYNTHESIS_REPORT、SOURCE_REVIEW／PLAN_REVIEW 人工確認、七天實作及中斷接續。
- **進階內容按需**：初次只複製 `PROMPT.md`；跨工具接力指示在當下產出；研究／課程細節需要時才看 `METHOD.md`，換對話時才用 `HANDOFF.md`。
- **驗證界線**：Draft PR 的文件、連結及三條使用路徑走查，不能替代真人完整七天成效驗證。

## 2026-11-12 — v0.2.3 / beginner-first entry and three-axis evidence clarity (untested)

### v0.2.3 follow-up｜README 不再嵌套另一份 Agent Prompt

修正公開上手流程的重複指令問題：`README.md` 原本提供一段要求 AI 重新讀取 Repo 的短 Prompt，與 `PROMPT.md` 正式啟動提示詞重複。現改為讀者直接進入 `PROMPT.md`、填寫學習主題並複製完整指令。README 只做介紹、導航、接力教學；未改研究流程、任何關卡或授權規則。這是 v0.2.3 內的 UX 修正，未另升版本。

**緣由**：使用者要讓沒有原專案背景的人直接拿公開 Repo 使用；v0.2.2 雖能停在 SOURCE_PACKAGE_READY，README 首屏仍用「AI 先排過課」的假設情境開場、Prompt 很長，且來源讀取標記、方法的可靠性與學習投入容易混成一種判斷。

**研究參考（閱讀原始 Repo README 及相關指南，借鏡原理，不複製其條目／證據評級）**：
- [byoungd/up](https://github.com/byoungd/up)：以目前問題和最小可執行動作作為入口；閱讀指南及 `learning-state` 最小模板讓讀者知道第一步留下什麼、下一步在哪裡恢復。
- [eternity4719/HowToLiveBetter](https://github.com/eternity4719/HowToLiveBetter)：把資料可核對性、行動成本和預期好處分開，不把證據等級當作必然效果或個人適用性。

**修訂**：
1. `README.md` 改用真實前提「免費教材散落不同平台和語言」，提供可直接複製的短啟動 Prompt、收到各階段結果時的下一動作，以及常見卡住時的恢復語句；完整主 Prompt 仍保留作為無法連 GitHub 的替代方案。
2. `PROMPT.md`、`RESEARCH_METHOD.md`、`SOURCE_LOG_TEMPLATE.md` 在**既有** R2／SOURCE_REVIEW 內區分「來源實際讀到多少」、「方法主張有多少證據及適用性」、「練習要投入多少時間／錢／工具、七天可以觀察什麼」，不引入新關卡，也不照搬外部 A/B/C 量尺。
3. 明確區分「原始資料無法開啟」的 `FAILED` 與「NotebookLM 導入失敗」的 `INGEST_RECEIPT`；修訂 `METHOD.md` 版本標示。

**不變**：預設 STANDARD + NOTEBOOKLM_FIRST、SOURCE_PACKAGE_READY、INGEST_REVIEW、SYNTHESIS_REPORT、SOURCE_REVIEW、PLAN_REVIEW、Day 1–7；QUICK_MODE 與 DIRECT_SYNTHESIS 仍需使用者明確選擇，人工批准與來源誠實邊界不變。

**驗證限制**：這次是文件改版和靜態讀回；沒有證明跨 AI 上手成功率或七天學習成效提高。公開版本可以邀請真人試用，但不應宣稱已驗證有效。

## 2026-11-12 — v0.2.2 / NotebookLM-first research handoff (untested)

**原因**：一次「30 秒料理短影片」測試在 v0.2.1 成功停在 SOURCE_REVIEW，卻在沒有 NotebookLM 匯入與跨來源統整的情況下，就自行完成來源比較。這符合當時主 Prompt 的「若想用 NotebookLM」文字，但未保留原本「先匯入、逐筆驗收，再整合研究」的核心方法。該次測試是使用者提供的 AI 輸出，不代表已驗證學習效果。

**變更**：
- 預設 `STANDARD + NOTEBOOKLM_FIRST`。R1 收尾先交完整來源 ID、原始 URL、讀取狀態、去重資訊與可複製匯入提示詞，停在 `SOURCE_PACKAGE_READY`。
- R2 依序要求筆記本逐筆 `INGEST_RECEIPT`，主 AI 的 `INGEST_REVIEW`，NotebookLM 跨來源 `SYNTHESIS_REPORT`，最後才由主 AI 發出 `SOURCE_REVIEW`。
- `RESEARCH_PROMPTS.md` 補上直接可用的 NotebookLM 匯入／統整兩段提示詞；`HANDOFF.md`、`SOURCE_LOG_TEMPLATE.md` 分別保留每個階段、匯入證據與未知。
- 使用者若無法或不想使用 NotebookLM，必須**明確選擇 `DIRECT_SYNTHESIS`**，由主 AI 使用可讀原始來源比較，不能聲稱已有筆記本收據。選擇 `QUICK_MODE` 不會自動跳過 NotebookLM。
- 研究可能跨多個工具與對話，仍不計入七天實作；SOURCE_REVIEW、PLAN_REVIEW 仍需學習者確認，NEED_SOURCES 的兩輪補搜上限不變。

**未驗證**：尚未由獨立 AI 真正從 SOURCE_PACKAGE_READY 完成 NotebookLM 匯入、帶回統整與完整七天學習；此改版僅為流程設計修正，非成效認證。

## 2026-11-12 — v0.2.1 / Grok Bot review consistency repair (untested)

**來源與性質**：依外部 Grok Bot 在 2026-11-12 提供的文件審查建議修正；Grok 的意見不是 Owner 核准，修改由 Owner 在對話中明確指示。本版本仍未完成真實七天學習或跨模型行為測試。

**三項 Must Fix**：
- **階段一致**：統一 `R0 定義 → R1 搜尋 → R2 驗收與跨來源比較 → SOURCE_REVIEW → R3 設計七天 → PLAN_REVIEW → R4 Day 1–7`；取消 RESEARCH_METHOD 裡同名但不同義的 R3/R4/R5。
- **QUICK_MODE 一致**：只有學習者明確提出，才縮減至最多 3 個來源；仍要簡版 SOURCE_REVIEW、等待確認、保留 PLAN_REVIEW 並標明信心較低。不能把未核對資料當已驗證。
- **來源標籤一致**：統一 `VERIFIED_FULL / REPORTED_FULL / PARTIAL / LINK_ONLY / FAILED / DUPLICATE / UNKNOWN`。沒有本輪實際讀回的全文或完整可用字幕不得標 VERIFIED_FULL；影片需另標視覺證據缺口。

**低成本改善**：補回財務／投資等高風險限制；在 README 說明研究可能跨多次對話、NotebookLM 與其他 AI 工具常需手動匯入與交接；NEED_SOURCES 需學習者同意，最多再補搜兩輪、每輪最多三個新來源；同步更新對外描述。個人研究起源敘述依既有公開內容保留，未新增私人資料。

**仍未知**：真實 AI 是否會遵守兩個停下來的關卡、來源核對品質及完整七天學習成效；文件一致性檢查不等於行為或教學成效實證。

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
