# Contributing Guide

ありがとうございます！貢献の方法と基準を以下にまとめます。

## 1. どのように貢献できますか
- 🐛 **バグ報告**: 「Bug report」フォームをご利用ください
- 💡 **機能要望**: 「Feature request」フォームをご利用ください
- 🧪 **改善 PR**: 小さな改善でも歓迎。まずは Issue で合意を取るとスムーズです

## 2. 開発の流れ（提案）
1. Issue を作成（再現手順 / 期待結果 / 実結果 を明記）
2. `feat/<topic>` または `fix/<issue-#>` ブランチを作成
3. 変更・テスト・ドキュメント更新
4. PR を作成（テンプレに従い、`Closes #<issue>` を記載）

## 3. コーディング規約（共通）
- **コミットメッセージ**: Conventional Commits（`feat: ...`, `fix: ...`, `docs: ...` など）
- **スタイル**: 言語に応じた標準 Linter/Formatter を推奨
  - Python: `ruff` / `black`（必要に応じ `isort`）
  - Markdown/YAML: 行末スペース削除、80–120 桁目処
- **ドキュメント**: ユーザー向けの変更は README/Usage を更新

## 4. Python リポ向けガイド（例: `whisper-srt`, `quantum-heat-engine-gkls`）
```bash
# 推奨: Python 3.10+
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -U pip
pip install -r requirements.txt  # 存在する場合
# Lint/Format（存在する場合）
ruff check . && black --check .
# Test（存在する場合）
pytest -q
```
- GPU/CUDA を使用する場合は、Issue で環境（GPU/Driver/CUDA/cuDNN）を明記

## 5. Web/Docs リポ向けガイド（例: `portfolio`）
- 破壊的変更はプレビュー URL / スクショを PR に添付
- HTML/CSS はアクセシビリティ（コントラスト/alt/ランドマーク）に配慮

## 6. レビュー基準（目安）
- 正確性（要件を満たすか）
- 安全性（セキュア／秘匿情報なし）
- 維持性（読みやすさ／テスト／ドキュメント）
- 影響範囲（互換性や性能）
