# プロジェクトステータス

## 概要
ブラウザで動く超シンプルなメモ帳。HTMLファイル1枚、localStorageで保存。

## 現在のバージョン / 状態
v0.0.0 - 設計完了、実装待ち

## 協業ステータス
- lead: Claude Code
- executor: Codex
- phase: design-complete
- handoff_ready: true
- next_owner: Codex
- final_owner: Claude Code
- updated_at: 2026-03-15 15:25 JST

## 設計（Codex向け実装指示）

### コンセプト
「超シンプル」がキーワード。余計な機能は一切不要。開いたら即書ける。

### 技術スタック
- HTML + CSS + JavaScript（単一ファイル `index.html`）
- データ保存: localStorage（外部API不要）

### 機能要件
1. **テキストエリア** — 画面いっぱいに広がる編集エリア
2. **自動保存** — 入力のたびにlocalStorageへ自動保存（debounce 300ms程度）
3. **ページ再読み込みで復元** — localStorageから読み込んで表示
4. **文字数カウント** — 右下あたりにさりげなく表示
5. **それだけ** — ボタンもメニューも不要

### デザイン要件
- ダークテーマ（目に優しい）
- 背景: `#1a1a2e` 系
- テキスト色: `#e0e0e0`
- フォント: monospace系（`'SF Mono', 'Fira Code', 'Consolas', monospace`）
- フォントサイズ: 16px
- テキストエリアはborder/outlineなし、画面全体
- 文字数カウントは半透明で控えめに
- パディング: 24px程度

### ファイル構成
```
index.html  ← これ1つだけ
```

## 直近の変更（最新を上に追記）
| 日付 | 変更内容 | 担当 |
|------|---------|------|
| 2026-03-15 | 設計完了、Issue作成、handoff_ready: true | Claude Code |

## 次にやること
- [ ] Issue #1: メモ帳の実装

## 現在の問題
なし

## ファイル構成
- `index.html` - メモ帳本体（未作成）
- `PROJECT_STATUS.md` - プロジェクト状態管理
- `CLAUDE.md` - Claude Code用ガイド
- `AGENTS.md` - Codex用ガイド

## テスト方法
- `index.html` をブラウザで開いて目視確認
- テキスト入力 → リロード → 復元されること

## デプロイ / リリース方法
- `index.html` をダブルクリックでブラウザで開く
