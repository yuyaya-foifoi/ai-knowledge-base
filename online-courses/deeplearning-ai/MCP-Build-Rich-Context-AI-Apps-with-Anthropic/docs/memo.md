# 概要
- 紹介されていた例は、github からタスクを理解してasanaでアサインするというもの
- MCPがないと、アプリごとに同じような機能を何度も実装することになり、労力やコストが分散・重複してしまう。統一的なプラットフォーム（＝MCP）があれば、これらの共通処理を一括管理・再利用可能にできる。
- 図の構造と意味
左側の3つのアプリ

MCP対応のAI Assistant

MCP対応のAI Agent

MCP対応のDesktop AppやIDE

これら異なるAIアプリケーションが…

⬇️

**中央の「Google Drive MCP Server」**を通じて…

⬇️

右側の「Google Drive」データへアクセスしています。


- ✅ AIアプリ開発者向け（AI application developers）
メリット：追加実装なしでMCPサーバーに接続可能

解説：アプリごとに個別にデータアクセスやツール統合を作らなくてよくなる → 開発が爆速化

✅ ツールやAPI開発者向け（Tool or API developers）
メリット：一度MCPサーバーを作れば、あらゆるアプリで使い回せる

解説：「書いたもの勝ち」で再利用性とスケーラビリティが最大化。1回の構築で多くのアプリに価値提供できる。

✅ AIアプリのユーザー向け（AI application users）
メリット：アプリの機能が豊富になる

解説：MCPに対応したアプリは、すぐに外部データや機能を使える → ユーザー体験が向上

✅ 企業・組織向け（Enterprises）
メリット：AI開発チーム間での責務分離が明確になる

解説：アプリ開発チーム vs データ接続チームを役割分担できる → 組織全体での生産性と保守性がUP


- ❓ 1. MCPサーバーは誰が作るの？
英語原文:
Who authors the MCP Server?
→ Anyone! Often the service provider itself will make their own MCP implementation...

日本語訳・要点:
→ 誰でも作れます！
特に、そのサービスの提供者自身（例：GoogleやNotionなど）が自分のMCPサーバーを提供するケースもあります。もちろん、自分でAPIをラップしてMCPサーバーを自作することも可能です。

❓ 2. MCPサーバーを使うのと、直接APIを呼び出すのは何が違う？
英語原文:
How is using an MCP Server different from just calling a service’s API directly?
→ MCP Servers provide tool schemas + functions. If you want to directly call an API...

日本語訳・要点:
→ MCPサーバーはツールのスキーマや関数を事前に提供してくれるので、自然言語から簡単にアクセスできます。
一方、直接APIを呼び出す場合は、自分で関数設計やリクエスト構築を全部やる必要があるため、開発負荷が高いです。

❓ 3. MCPサーバーとツールって同じものじゃないの？
英語原文:
Sounds like MCP Servers and tool use are the same thing.
→ MCP Servers provide tool schemas + functions already defined for you.

日本語訳・要点:
→ 一見似ているけれど、MCPサーバーはツールのスキーマや実行関数があらかじめ定義されているのが特徴です。
つまり、MCPサーバーはツールを“使いやすくするためのラッパー”のような存在です。

✅ 全体のまとめ
MCPサーバーとは、API呼び出しやツール連携を標準化・抽象化して、アプリやエージェントが自然言語で簡単に扱えるようにする仕組み。
その作成者も使い方も自由度が高く、開発を効率化します。

