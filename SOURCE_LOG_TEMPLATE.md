# 來源清單、匯入驗收與主張證據表（複製填寫）

> 這份表不要求每欄都有值；無資料寫 UNKNOWN。將個人隱私內容保留在私人工作區，不要貼公開 Issue。

## 研究範圍

- 主題：
- 起點／學習目標（候選）：
- 需要回答的研究問題：
- 搜尋語言與平台：
- 搜尋日期：
- 研究模式（STANDARD / QUICK_MODE，需使用者明確提出 QUICK_MODE）：
- 研究路線（預設 NOTEBOOKLM_FIRST／使用者明確選擇 DIRECT_SYNTHESIS）：
- 本輪最多新增幾個來源／何時停止（一般首次最多 6–12，QUICK_MODE 最多 3）：
- NEED_SOURCES 已使用的補搜輪次（0／1／2，最多 2 輪、每輪最多 3 個新來源）：
- 收集者（本人／AI 工具／他人）：
- 核對者與日期：

## 候選來源

| ID | 原始標題／作者 | 語言、年份 | 類型與網址 | 為什麼選 | 讀取狀態 | 片長／字幕／畫面 | 來源強度／限制 |
|---|---|---|---|---|---|---|---|
| S01 | | | | | UNKNOWN | | |
| S02 | | | | | UNKNOWN | | |

來源讀取狀態：
- `VERIFIED_FULL`：本輪研究者實際開啟並核對完整文本或完整可用字幕，記錄核對者與日期；不表示影片畫面已看過
- `REPORTED_FULL`：其他 AI 回報取得完整，但本次未獨立核對
- `PARTIAL`：只有部分文章／字幕／課程
- `LINK_ONLY`：只有 URL、搜尋摘要或網頁標題，未核對原始完整內容
- `FAILED`：無法匯入或開啟
- `DUPLICATE`：相同原始內容的另一個形式／另一份摘要
- `UNKNOWN`：讀取範圍無法確認

影片加註 `VISUAL_UNCHECKED`、`CAPTIONS_UNAVAILABLE`、`DEMO_VISIBLE`（實際檢查過示範）等，**字幕完整不代表看過示範畫面**。

來源類型：原始作品／本人自述／第三方報導／官方文件／研究論文／專家方法／AI 二次整理／學習者實作證據。類型不是全域信用分數，須依主張判定適用性。

## SOURCE_PACKAGE_READY｜待匯入來源包

- 來源包完成時間：
- 選定來源清單及完整原始 URL（不能只有標題或 AI 內部引用編號）：
- 重複／無法取得／影片 VISUAL_UNCHECKED：
- 可直接複製的 NotebookLM 匯入提示詞位置：
- 交接狀態（PENDING / HANDOFF_READY / DIRECT_SYNTHESIS_CHOSEN）：

## INGEST_RECEIPT｜NotebookLM 匯入與核對

**注意**：下面是筆記本「平台匯入狀態」，與上面的原始來源「讀取狀態」不同。筆記本接受 URL，不代表已核對全文；NotebookLM 讀到字幕，不代表看過影片畫面。

| ID | 對應原始 URL | NotebookLM 來源名稱 | 平台匯入（成功／部分／失敗／未知） | 實際可見內容／核對方式 | 缺少的字幕／畫面／子頁 |
|---|---|---|---|---|---|
| S01 | | | UNKNOWN | | |

## INGEST_REVIEW → SYNTHESIS_REPORT

- 原來源數：
- 匯入成功／部分／失敗／未知的來源數：
- 筆記本中的獨立來源數（同一作品不同形式去重）：
- 仍未確認的字幕、畫面、子頁與全文：
- INGEST_REVIEW 由誰何時做、憑什麼核對：
- **完整 NotebookLM 跨來源統整提示詞是否已交付**：
- SYNTHESIS_REPORT 是否已由筆記本實際生成並帶回（YES / NO / UNKNOWN）：
- SYNTHESIS_REPORT 定位及可回查來源／引用：
- **若採 DIRECT_SYNTHESIS**：使用者明確選擇的紀錄、NotebookLM 未使用、主 AI 實際可讀來源及限制：

## 研究主張對照

| 主張／可重做的技巧 | 支持的原始來源與定位 | 反例或不同解釋 | 目前判斷 | 下一步如何驗證 |
|---|---|---|---|---|
| | | | CANDIDATE | |

用語：
- `OBSERVED`：來源可直接支持的描述，不等於普遍有效
- `SELF_REPORTED`：經營者／講師自己說的結果
- `EXPERT_METHOD`：教學方法論，不等於學員已進步
- `AI_SUMMARY`：二次資料／需追到原始內容
- `CANDIDATE`：綜合假說
- `UNKNOWN`：沒有足夠資料

## SOURCE_REVIEW 結案

此關卡只有在 NOTEBOOKLM_FIRST 的 `INGEST_RECEIPT`、`INGEST_REVIEW`、`SYNTHESIS_REPORT` 已完成、或使用者明確選擇 DIRECT_SYNTHESIS 並如實記錄後，才能提交。R1 的來源包不是 SOURCE_REVIEW。

- 可用獨立來源數（同一講座的文字與影片算一個觀點）：
- 可用技能示範／真實案例：
- 內容重複或缺畫面：
- 已知最大偏差或反例：
- 尚缺重要來源（最多 3 項）：
- 本輪停止／繼續條件（NEED_SOURCES 須使用者同意，補搜不能超過兩輪）：
- 建議狀態：READY / PARTIAL_READY / NEED_SOURCES / STOP
- **學習者決定**（未回覆先留 PENDING）：
- 允許進行七天課程設計了嗎？（YES / NO / PENDING）：
