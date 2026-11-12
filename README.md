# 想學什麼？先找懂的人怎麼做，再讓 AI 陪你練七天
### 7-Day AI Learning Loop · Research-first

> **v0.2.2｜公開試用、尚未實測。** 一套可複製的「跨來源研究 → 課程設計 → AI 七天實作陪跑」方法。不是七天精通或收入保證。

## 你可能遇過這種情況

你問 AI「我想學 Threads 經營／吉他／外語／做一個小型服務，幫我設計七天課程」，它很快就交出漂亮的課表，但沒有查誰真正做過、哪些長影片有完整示範、能否學到核心技能、會不會只有成功者的自述。

**這個 Repo 的主張是：先把資料找對、來源核對好，再讓 AI 設計真正能動手做的七天。**

## 先用一個 Prompt 開始

**[開啟／複製 Research-first 主提示詞 →](PROMPT.md)**

1. 告訴 AI 想學或想試的主題（其餘資訊可留白）。
2. AI 搜尋**完整長影片、文章、官方文件、必要時的 X／Threads 真實案例**，將每份原始 URL、讀取狀態整理成 `SOURCE_PACKAGE_READY`。**此處先停下**，交給你可複製的 NotebookLM 匯入提示詞。
3. **NOTEBOOKLM_FIRST（預設）**：由你或有權限的工具，將已挑選的來源匯入 NotebookLM；將每筆匯入結果回傳主 AI。
4. **INGEST_REVIEW**：主 AI 比對實際匯入成功、失敗、只有字幕、缺畫面的情況；再給你 NotebookLM 跨來源統整提示詞。NotebookLM 依來源找共同方法、歧見、反例與可練習的技巧，你再帶回統整報告。
5. **SOURCE_REVIEW**：主 AI 根據匯入收據與跨來源報告審查證據。此時才提出 READY／PARTIAL_READY／NEED_SOURCES／STOP，等你決定。
6. AI 根據你接受的研究結果設計七天路線圖；**PLAN_REVIEW** 確認後，才開始 Day 1。
7. 每天練習、提交作品、讓 AI 批改後自己重做；Day 7 比較起點與成果。

**研究階段不算七天練習時間**：依主題與來源可讀性，可能需要數次對話，甚至跨幾天完成；NotebookLM 匯入、Grok／X 與 Meta AI／Threads 查找通常需要你自行切換工具、貼上研究提示詞並帶回報告。這是可以跨多個 AI 工具手動接力的**工作流程與提示詞**，不是會自行瀏覽所有平台、同步 NotebookLM、發文或寄提醒的自動化服務。

**沒有 NotebookLM 也能用，但不會默默跳過**：預設 `NOTEBOOKLM_FIRST`。若你無法使用或不想使用，請明確回覆「選擇 `DIRECT_SYNTHESIS`」，主 AI 才可根據它實際取得的來源直接統整，並標記研究路線和限制。它仍要停在 SOURCE_REVIEW 與 PLAN_REVIEW，不得把 AI 摘要當原始資料。

**QUICK_MODE（必須由使用者明確要求）**：只把研究來源縮到最多 3 個，不跳過來源包、匯入驗收或正式研究審查；標示證據信心較低。預設 STANDARD 首輪最多 6–12 個互補來源。NEED_SOURCES 經使用者確認最多再補搜兩輪，每輪最多新增 3 個來源，仍不足就縮小題目或停止。

## 它從哪裡來？

原本是在研究「閒人出租的個人品牌」：找台灣 Threads 起步案例、日本經營者長訪談、英文實作工作坊，請 Meta AI／Grok 補查難以穩定取得的 Threads／X 貼文，再匯入 NotebookLM 比對成功者偏差、價格與顧客需求；最後才決定怎麼設計七天課。

**重要的不是那個主題，而是從「搜尋素材」到「證據審查」再到「可練習方法」的過程。** 研究歷程的通用版與限制見 [ORIGIN.md](ORIGIN.md)。

## 核心地圖

```text
定義想學的主題
  → R0 研究問題／範圍
  → R1 跨媒介搜尋、去重、核對來源 → SOURCE_PACKAGE_READY（停下）
  → NOTEBOOKLM_FIRST：人工／授權工具匯入 → INGEST_REVIEW
  → R2 NotebookLM 跨來源統整 → 帶回 SYNTHESIS_REPORT
  → SOURCE_REVIEW（使用者確認）
  → R3 依研究設計七天路線圖 → PLAN_REVIEW（使用者確認）
  → R4 Day 1–7 練習、批改、重做、驗收與回顧
```

## 檔案導覽

| 檔案 | 你需要的時候 |
|---|---|
| **[PROMPT.md](PROMPT.md)** | 一鍵啟動，預設交付 NotebookLM 來源包與兩次研究接力 |
| [RESEARCH_METHOD.md](RESEARCH_METHOD.md) | 跨語言找完整長影片／文章／社群案例、NotebookLM 來源驗收、研究停損 |
| [RESEARCH_PROMPTS.md](RESEARCH_PROMPTS.md) | 來源包之後給 Gemini／NotebookLM 的逐筆匯入提示詞、跨來源統整提示詞，以及 Grok／X、Meta AI／Threads 子任務 |
| [SOURCE_LOG_TEMPLATE.md](SOURCE_LOG_TEMPLATE.md) | 逐筆來源、字幕／影片畫面缺失、AI 二次摘要、反例與 SOURCE_REVIEW |
| [METHOD.md](METHOD.md) | 把研究轉成七天技能訓練、批改、teach-back、驗收 |
| [DAILY_REVIEW.md](DAILY_REVIEW.md) | 真實成果、本人與 AI 分工、每日改進與 Day 7 前後測 |
| [HANDOFF.md](HANDOFF.md) | 跨工具／跨對話接續，保留來源與關卡狀態 |
| [ORIGIN.md](ORIGIN.md) | 方法起源、為何重視完整來源與真實證據 |
| [SOURCES.md](SOURCES.md) | 公開參考線索，非唯一教材／非成效證明 |
| [CHANGELOG.md](CHANGELOG.md) | 版本的設計變更 |
| [LICENSE](LICENSE) | MIT（只涵蓋 Repo 原創內容） |

## 每個主題不一定都要找 Grok 或兩小時影片

學程式可能以官方文件與實機示範為主；學吉他可能以演奏示範、練習錄音與安全動作為主；研究 Threads 經營才可能需要日本、英文訪談、X／Threads 個案。**找的是必要證據，不是把工具清單硬跑一遍。**

沒有某個平台的存取權也能使用：主 AI 需誠實標示無法讀取，並提供精確的人工搜尋／匯入提示詞；但未得到使用者明確選擇 `DIRECT_SYNTHESIS` 前，不可略過 `SOURCE_PACKAGE_READY` 直接完成研究。來源狀態統一使用 `VERIFIED_FULL / REPORTED_FULL / PARTIAL / LINK_ONLY / FAILED / DUPLICATE / UNKNOWN`；只有本輪實際核對全文或完整可用字幕才能標 `VERIFIED_FULL`，別把搜尋摘要當全文。影片如果只讀到字幕、未檢查操作畫面，必須另外標 `VISUAL_UNCHECKED`，不能教成親眼看過的示範。

## 公開試用與限制

- **尚未驗證成效**：公開是讓任何人可以先用與回饋，不代表已有人成功完成七天課。
- **沒有私有資料**：不公開作者個人研究原文、客戶資料、完整第三方逐字稿或私人課程。
- **證據先行**：成功案例是案例、專家說法是方法候選、真實學員的成果才是學習結果。
- **沒有授權就不對外動作**：發文、私訊、付費、公開成果、改 Repo 都要另外同意。
- **高風險主題**：不以七天練習替代醫療、心理健康、法律、財務或投資專業建議、其他資格與安全要求；不保證交易或收益。

要提建議可用 [GitHub Issues](https://github.com/guoyutw/7day-ai-learning-loop/issues)；請只分享去識別化的研究差異、使用障礙及成果，不要上傳私人對話。

> 繁體中文為主要版本；歡迎後續提出多語翻譯。公開 v0.2.2 是方法候選，不是已獲科研驗證的產品。
