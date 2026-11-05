# 注音鍵盤誤植解碼

這支 Agent Skill 幫助 AI 助理辨認「忘了切到注音輸入法」打出的字串。例如 `2jo4` 對應 `ㄉㄨㄟˋ`，在中文對話裡可能是想打「對」。助理會用大千式鍵盤對照表拆音，再根據上下文提出猜測，讓你確認。

## 在 Codex 使用

1. 下載這個儲存庫並解壓縮，將資料夾命名為 `zhuyin-typo-decode`。
2. 將整個資料夾放進專案的 `.agents/skills/`，或家目錄的 `~/.agents/skills/`。保留 `SKILL.md` 和 `references/` 的相對位置。
3. 在 Codex 試一句「用 `$zhuyin-typo-decode` 幫我解讀 `2jo4`」。

[Codex 技能安裝位置](https://developers.openai.com/api/reference/cli)

## 解碼範例

| 英數模式打出的字串 | 拆音 | 可能的原意 |
| --- | --- | --- |
| `2jo4` | ㄉㄨㄟˋ | 對 |
| `w94cl3xk7` | ㄊㄞˋ ㄏㄠˇ ㄌㄜ˙ | 太好了 |

同音字與省略空格的一聲音節可能有多種解讀。技能會依中文語境提出候選，並避開看得出是網址、程式碼、型號或驗證碼的字串。

- [技能指示](SKILL.md)
- [大千式鍵盤對照表](references/keyboard-map.md)
