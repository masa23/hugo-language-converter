# Hugo Language Convert (hlc)

## これは何？

HugoのMarkdownをさくらのAI Engineを使って変換するためのツールです。  
自分のブログの記事を英語に翻訳するために作りました。

## 使い方

1. さくらのAI EngineのAPIキーを取得します。
2. config.yamlを編集します。
3. `hlc`を実行します。

```bash
$ hlc -input input.md -output output.md

# or

$ cat input.md | hlc > output.md
```

## config

```yaml
---
AIEngine:
  APIToken: "your-api-token"
  Model: "gpt-oss-120b"
  MaxTokens: 1000
Prompt: |
  # Command
  * Convert the Markdown of a hugo article according to instructions
  * Do not convert within comment blocks
  * Output should be in Markdown only

  # Instructions
  * 記事を英語に翻訳する
```

Promptに変換の指示を記述します。
