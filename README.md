# 網路上已經有免費教材，讓 AI 幫你找到、整理，再陪你練七天

### 7-Day AI Learning Loop · Research-first

> **v0.2.3｜公開試用，學習成效尚未驗證。** 把散落在不同語言、YouTube、專家文章與公開教材的知識，整理成屬於你的七天實作課程。不保證七天精通，也不代替專業資格或判斷。

## 從這裡開始

**只做一件事：選一項你想學的技能，複製下面這段到你常用的 AI。** 不必會寫程式，也不用先讀完整個 Repo。

```text
我想用這套公開方法，讓 AI 陪我學習：
https://github.com/guoyutw/7day-ai-learning-loop

我想學：【填入主題，例如用手機剪一支 30 秒影片】
我目前的程度：【初學者／已有一點基礎】
每天可投入：【例如 30 分鐘】

請讀取 main 分支最新的 PROMPT.md、RESEARCH_METHOD.md、
RESEARCH_PROMPTS.md、SOURCE_LOG_TEMPLATE.md，遵守目前版本的完整流程。
使用 STANDARD + NOTEBOOKLM_FIRST，先搜尋、篩選跨語言免費教材，
給我含原始網址的 SOURCE_PACKAGE_READY 和可直接複製的 NotebookLM 匯入提示詞，
然後停止，等我實際匯入後再接續。不要現在就排七天課表。
若無法讀取 GitHub 文件，請明說需要我貼上哪份文件，不要假裝已讀。
```

> **AI 讀不到 GitHub？** 打開 [完整主提示詞 PROMPT.md](PROMPT.md)，複製整段貼給 AI，再補上你想學的主題即可。不要讓它憑空假裝讀過 Repo。

## AI 第一次回覆後，你要做什麼？

| 收到什麼 | 你要做的事 |
|---|---|
| **SOURCE_PACKAGE_READY**：來源網址清單、讀取限制、匯入提示詞 | 複製它給 Gemini；如果沒有直接匯入權限，就在 [NotebookLM](https://notebooklm.google.com/) 自己建立筆記本並匯入。**不用先看完每份教材。** |
| **INGEST_RECEIPT**：哪些材料真的匯入成功、哪些失敗 | 貼回原本的 AI 對話；它會核對並產生下一段 NotebookLM 統整提示詞。 |
| **SYNTHESIS_REPORT**：NotebookLM 比較教材的共通方法、反例與缺口 | 貼回原本 AI；它才會交正式 **SOURCE_REVIEW**，請你決定資料夠不夠。 |
| **PLAN_REVIEW**：七天課程草案 | 確認時間、難度與成果標準後才開始 Day 1。 |

每次只操作目前這一步，不必預先理解所有英文標籤。**研究可能要花數次對話，七天是後面的實作時間，不包含找資料。** 這是跨工具、部分需要手動複製的流程，並不是自動操作所有平台的服務。

**如果卡住：**
- AI 直接產生七天課表：回覆「請回到 `SOURCE_PACKAGE_READY`，先給我來源包與 NotebookLM 匯入提示詞」。
- Gemini 沒有 NotebookLM 操作權限：自己將指定來源加進 NotebookLM，記下成功／失敗，再貼回原 AI；不能讓 AI 假稱已匯入。
- 不想使用 NotebookLM：可以明確對主 AI 說「我選擇 `DIRECT_SYNTHESIS`」，它才會直接統整**實際讀過**的來源；兩次正式確認仍保留。
- 研究時間或精力有限：可明確要求 `QUICK_MODE`，來源縮到最多 3 個，但仍保留 NotebookLM 接力（除非另選 `DIRECT_SYNTHESIS`）、SOURCE_REVIEW 與 PLAN_REVIEW。

## 這套方法在做什麼？

不是把 AI 想出來的七堂課直接當教材。網路上已有完整工作坊、公開長影片、作者的實際方法與免費教學文章，卻可能散落在不同國家和平台。

研究要先找出值得讀的資料，確認真正取得了什麼，再利用 NotebookLM 比較，而不是把「找到連結」當成「看完內容」。**最後讓 AI 把有限且可追溯的資料轉成七天內可以做、可以提交作品、可以接受回饋的練習。**

原本的研究題目是「閒人出租 × 個人品牌」：從台灣 Threads、日本經營者訪談、英文工作坊蒐集候選資料，請 Meta AI／Grok 協助查找難以直接存取的貼文，再經 Gemini／NotebookLM 研究及三輪課程設計審查。那是方法的起源，**不代表已完成七天試教或證明學員進步**。詳見 [ORIGIN.md](ORIGIN.md)。

## 研究看三件不同的事

| 判斷 | 問什麼 | 例子 |
|---|---|---|
| **讀取狀態** | AI 真的取得了多少來源內容？ | 文章讀完可標 `VERIFIED_FULL`；只有連結不能。 |
| **方法依據** | 內容能支持什麼主張？ | 作者提出的寫作技巧是**待驗證的方法**，不是「七天保證學會」。 |
| **投入與成果** | 你要花多少時間／工具？七天能觀察什麼？ | 每次練 20 分鐘，提交一版作品；是否改善，須和本人起點比較。 |

這三件事互不替代：**讀過完整文章 ≠ 方法有效；證據充分 ≠ 這個人值得投入所有時間。** 我們不照搬外部 Repo 的 A/B/C 證據分級或 CP 值公式，而是讓每項主要練習說清楚來源、適用條件、投入與可觀察結果。

## 流程與限制

```text
R0 定義想學的事
 → R1 跨語言找免費教材 → SOURCE_PACKAGE_READY（停下）
 → NotebookLM 匯入 → INGEST_RECEIPT
 → 主 AI 做 INGEST_REVIEW（停下，給統整提示詞）
 → NotebookLM 做 SYNTHESIS_REPORT
 → 主 AI 做 SOURCE_REVIEW（等你確認）
 → R3 設計七天 → PLAN_REVIEW（等你確認）
 → R4 Day 1–7：自己練習、回饋、重做、前後比較
```

- **來源選擇**：STANDARD 首輪最多 6–12 個互補來源，不為湊數；QUICK_MODE 要明確要求，最多 3 個。NEED_SOURCES 需同意，最多再補搜兩輪，每輪最多新增 3 筆。
- **NotebookLM-first 是預設**：沒有匯入收據與統整報告，就不能假稱完成該流程；不用 NotebookLM 須使用者明確選擇 DIRECT_SYNTHESIS。
- **證據誠實**：來源狀態用 `VERIFIED_FULL / REPORTED_FULL / PARTIAL / LINK_ONLY / FAILED / DUPLICATE / UNKNOWN`。影片字幕完整不代表看過畫面；未核對示範要標 `VISUAL_UNCHECKED`。任何 AI 二次整理都不能冒充原始作品。
- **不是所有主題都要搜社群**：程式可先看官方文件；樂器更需要實際演奏畫面；研究個人品牌才可能需要 X／Threads 個案。
- **隱私、安全與授權**：不公開私人對話、客戶或他人付費教材；醫療、法律、財務、危險操作等不以七天課取代專業判斷。發文、私訊、交易或變更外部資料要另經同意。
- **尚未證實成效**：目前只是可試用的公開方法，沒有跨人群、跨 AI 工具的完整七天成效證據。

## 想查詳細規則，再打開這些檔案

| 檔案 | 用途 |
|---|---|
| **[PROMPT.md](PROMPT.md)** | 完整的 AI 啟動指令與每個停止關卡 |
| [RESEARCH_METHOD.md](RESEARCH_METHOD.md) | 選來源、判斷可靠性、NotebookLM 接力與停損 |
| [RESEARCH_PROMPTS.md](RESEARCH_PROMPTS.md) | Gemini／NotebookLM 匯入與統整提示詞、其他研究子任務 |
| [SOURCE_LOG_TEMPLATE.md](SOURCE_LOG_TEMPLATE.md) | 來源、匯入、主張、限制與 SOURCE_REVIEW 的進階紀錄表 |
| [METHOD.md](METHOD.md) | 七天實作、批改與學習驗收 |
| [DAILY_REVIEW.md](DAILY_REVIEW.md) | 本人作品、AI 協助範圍、前後比較 |
| [HANDOFF.md](HANDOFF.md) | 跨平台或新對話時，保留目前階段與未完成工作 |
| [ORIGIN.md](ORIGIN.md) | 方法起源與限制 |
| [SOURCES.md](SOURCES.md) | 公開研究線索 |
| [CHANGELOG.md](CHANGELOG.md) | 版本修正歷史 |
| [LICENSE](LICENSE) | MIT：本 Repo 原創內容授權 |

**歡迎試用回報**：可開 [GitHub Issue](https://github.com/guoyutw/7day-ai-learning-loop/issues)，簡單寫「想學的主題、使用哪個 AI、卡在哪一個步驟」即可；不必上傳私人筆記或完整對話。

> 繁體中文為主要版本。公開 v0.2.3 是方法候選，不是經驗證的教學產品。