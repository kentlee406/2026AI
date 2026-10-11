# 第一章  Al Agentic Coding Tool課前知識

[← 回到目錄](../README.md)

## 大綱

## AI類型的開發工具有哪些
### 對話式AI介面
* 優點: 容易使用、容易了解知識。
* 缺點: 無法存取程式碼內容。

### IDE類型整合工具
* 優點：可讀取專案程式碼、好上手、自動補全程式碼
* 缺點：非模型廠商直接推出

### 命令列工具
* 包括OpenAI Codex, Anthropic Claude Code, Gemini CLI, GitHub Copilot CLI
* 優點：由主流廠商推出，與模型整合度較高、自定義程度較高
* 缺點：使用指令操作，學習曲線較高
```
舉例來說，當你使用 IDE 整合工具（如 Cursor）時，它的功能大多是內建好的，你只能在它提供的介面內操作。

但如果使用 CLI 工具（如 Claude Code），你可以透過設定檔自定義工作流程例如：指定 AI 在修改程式碼前必須先跑測試、限制它只能修改特定資料夾的檔案、或是串接外部工具來擴充功能。CLI 給你更多控制權，但也需要更多設定。
```

## AI 關鍵字
### Model
* 開發過程中，較常使用Codex模型。
* 模型的價格與品質有所不同。

### Token
* AI理解文字的單位，每個英文單字約占1~3個Token，中文則是每個字1~2個Token。可參閱OpenAI Tokenizer：https://platform.openai.com/tokenizer

### Context
* 微觀層面：逐字推理的自我回歸模型，AI 是一個字一個字地預測下一個字，就像自動完成功能一樣
* 宏觀層面：歷史對話的載入
* Context的影響：
  * Prompt的輸入會影響產出。
  * 確保文章的前後關聯性。
  * 認識 Context Length 的限制： 每個模型都有其「記憶力」的上限（以 Token 計算）。一旦對話歷史或文件內容超過這個上限，模型就會開始「忘記」最開始的內容，導致回應出錯或偏離主題。
* 什麼情況會超過 Context Length
  * 長時間的連續對話
  * 複雜的程式碼庫理解
  * 外部資源的引用
* Context Length超過怎麼辦？
  * 創建新的對話：代表先前的對話要完全重來
  * 壓縮上下文：可以分析對話以識別值得保留的關鍵資訊，並創建先前互動、決策和程式碼變更的簡潔摘要。但依然可能造成精準度下降。

### Prompt
* 說明清楚要做或不要做的事情。

## [AI服務定價](https://liberating-turtle-5a2.notion.site/AI-3246a2468518806d89a5ca9cd2aad59d)

## [常見終端機指令](https://liberating-turtle-5a2.notion.site/3246a24685188036a818e8c882a84b81)

## WSL2 (Windows Subsystem for Linux 2)
開發者長期面對一個問題：大多數的伺服器都跑 Linux，但很多人的電腦是 Windows。兩個系統的行為不太一樣，導致「我電腦上跑得好好的，上線就壞掉」這種狀況很常見。WSL2 讓你在 Windows 上就能用 Linux 的環境開發，減少這個落差。

https://liberating-turtle-5a2.notion.site/Windows-WSL2-3246a246851880b4958ef4a2a3a1f306
https://liberating-turtle-5a2.notion.site/Windows-WSL2-3246a246851880ea9ffacaf37c524e6c

## 安裝 Claude Code 與 Codex

