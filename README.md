# AI Knowledge Base

このリポジトリは、DeepLearning.AIのオンラインコースの学習内容を整理・保存するナレッジベースです。

## 📚 コース一覧

### 1. MCP - Build Rich Context AI Apps with Anthropic

| 項目 | 内容 |
|-----|------|
| **コース概要** | Model Context Protocol (MCP) を使用してリッチなコンテキストを持つAIアプリケーションを構築する方法を学習 |
| **場所** | `online-courses/deeplearning-ai/MCP-Build-Rich-Context-AI-Apps-with-Anthropic/` |
| **ドキュメント** | `docs/mcp_architecture.md` - MCP アーキテクチャの詳細解説（日本語）<br>`docs/memo.md` - コース学習メモ、実装例、Q&A |
| **主要トピック** | • MCPアーキテクチャ（Host, Client, Server, Protocol）<br>• リソース管理（Direct vs Templated）<br>• プロンプトテンプレート<br>• 通信ライフサイクル<br>• 転送方法（stdio, HTTP+SSE, Streamable HTTP） |
| **学習メリット** | 開発者、ツール作成者、ユーザー、企業それぞれの観点でのMCP活用メリットを理解 |

### 2. Long-term Agentic Memory with LangGraph

| 項目 | 内容 |
|-----|------|
| **コース概要** | LangGraphを使用して長期記憶を持つエージェントシステムを構築する方法を学習 |
| **場所** | `online-courses/deeplearning-ai/long-term-agentic-memory-with-langgraph/` |
| **ドキュメント** | `docs/memo.md` - 3つのメモリタイプの解説とメールアシスタント実装説明 |
| **技術スタック** | LangChain, LangGraph, LangMem, OpenAI/Anthropic, Vector Embeddings |
| **主要概念** | **意味記憶**: 事実とユーザー情報の保存<br>**エピソード記憶**: 過去の経験と学習例<br>**手続き記憶**: 指示と行動パターン |

## 📖 レッスン詳細

| レッスン | ファイル | 実装内容 | 主要機能 |
|---------|---------|---------|---------|
| **Lesson 2** | `lesson2.ipynb` | **ベースラインメールアシスタント** | • メールトリアージ（無視/通知/返信）<br>• 基本エージェントツール<br>• LangGraph状態管理<br>• ルールベースの処理 |
| **Lesson 3** | `lesson_3.ipynb` | **意味記憶付きメールアシスタント** | • 永続メモリストレージ<br>• メモリ管理ツール<br>• ベクトル埋め込みによる意味検索<br>• セッション間での文脈保持 |
| **Lesson 4** | `lesson_4.ipynb` | **意味記憶 + エピソード記憶** | • Few-shot学習<br>• 過去の分類例からの学習<br>• Human-in-the-loopフィードバック<br>• 例ベース学習による精度向上 |
| **Lesson 5** | `lesson_5.ipynb` | **全3種類のメモリ統合** | • 手続き記憶：動的指示更新<br>• マルチプロンプト最適化<br>• 永続的行動修正<br>• 言語・トーン適応 |

## 🛠️ 技術実装

| コンポーネント | 技術 | 用途 |
|--------------|------|------|
| **状態管理** | LangGraph | エージェントオーケストレーション |
| **LLM統合** | LangChain | ツール管理とLLM連携 |
| **言語モデル** | OpenAI/Anthropic | 異なるコンポーネント用 |
| **意味検索** | Vector Embeddings | セマンティック検索機能 |
| **データ検証** | Pydantic | 構造化出力とバリデーション |
| **メモリストレージ** | InMemoryStore/LangMem | 永続メモリ管理 |

## 📋 コア機能

| 機能カテゴリ | 詳細 |
|-------------|------|
| **メール自動化** | • 自動トリアージ<br>• 文脈に応じた返信生成<br>• カレンダー統合 |
| **学習・適応** | • ユーザーフィードバックからの永続学習<br>• 行動パターンの修正<br>• 多言語コミュニケーション対応 |
| **メモリ管理** | • 意味記憶：事実と情報<br>• エピソード記憶：過去の経験<br>• 手続き記憶：行動指示 |

## 🎯 学習パス

このリポジトリは、基本的なルールベースエージェントから、学習・適応が可能な高度なメモリ機能付きAIアシスタントまでの包括的な学習パスを提供しています。

**進行順序**: 
Lesson 2 → Lesson 3 → Lesson 4 → Lesson 5

各レッスンは前のレッスンの機能を拡張し、最終的に3つのメモリタイプを統合した完全なエージェントシステムを実装します。