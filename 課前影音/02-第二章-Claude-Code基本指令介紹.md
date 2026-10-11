# 第二章  Claude Code 基本指令介紹

[← 回到目錄](../README.md)

講義：[Claude Code 基本指令介紹](https://liberating-turtle-5a2.notion.site/Claude-Code-3266a246851880009d4aee830e155562?source=copy_link)

## Claude Code相關指令

1. `/help`：檢視目前有哪些指令
2. `/model`：檢視目前使用的模型 (推薦使用：Opus, Sonnet)
3. `/init`：專案初始化 (建立CLAUDE.md)
4. 可以搭配 `@` 指定在哪一個檔案進行開發
5. 使用 `/status` 檢視當前用量
6. 使用 `/context` 檢視目前的用量佔比
7. 使用 `/clear` 清除目前對話
8. 使用 `/resume` 回覆先前的對話 

* 每次完成指令建議commit

## Claude Code Plan Mode 
1. 使用Shift+Tab切換
2. 檢視 Claude 提出的計畫內容，與 Claude 來回討論、調整方向
3. 在開發過程中追加新條件，觸發 AskUserQuestion (當有不清楚的地方可以跟我討論)
4. 回答 Claude 的問題後，開始開發
5. 儲存後使用 /compact 壓縮對話
6. 開發完成，請 Claude 進行 Commit

## Claude Code設定
