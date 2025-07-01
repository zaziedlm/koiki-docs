# KOIKI-FW ドキュメントサイト

KOIKI-FW（FastAPIベースのエンタープライズ向けWebアプリケーション基盤フレームワーク）v0.5.0 の公式ドキュメントサイトです。

## 📖 概要

このプロジェクトは、[MkDocs](https://www.mkdocs.org/) と [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) を使用して、KOIKI-FWの技術仕様書や導入ガイドを美しく整理し、GitHub Pagesで公開しています。

### ドキュメント内容

- **KOIKI-FW v0.5.0 機能設計・構成ガイド**: フレームワークの詳細な技術仕様
- **導入・セットアップガイド**: Docker Composeを使った環境構築
- **セキュリティ監査**: セキュリティ脆弱性の対策と修正内容
- **エンタープライズ依存性管理戦略**: 本格運用のための依存関係管理

## 🚀 クイックスタート

### 必要な環境

- Python 3.11.7
- Poetry（依存関係管理）

### ローカル環境でのドキュメント確認

```bash
# 依存関係のインストール
poetry install

# 開発サーバーの起動
poetry run mkdocs serve
```

ブラウザで `http://127.0.0.1:8000` にアクセスしてドキュメントを確認できます。

### GitHub Pagesへのデプロイ

```bash
# 静的サイトのビルド
poetry run mkdocs build

# GitHub Pagesへのデプロイ
poetry run mkdocs gh-deploy
```

## 📁 プロジェクト構成

```
koiki-docs/
├── docs/                          # ドキュメントソース
│   ├── index.md                   # トップページ
│   ├── design_kkfw_0.5.0.md      # 機能設計・構成ガイド
│   ├── README-deploy.md           # 配備ガイド
│   ├── SECURITY_AUDIT_COMMANDS.md # セキュリティ監査
│   └── ENTERPRISE_DEPENDENCY_STRATEGY.md # 依存性管理戦略
├── site/                          # ビルド済み静的サイト
├── mkdocs.yml                     # MkDocs設定ファイル
├── pyproject.toml                 # Python依存関係設定
└── .python-version                # Python バージョン指定
```

## 🔧 設定

### MkDocs設定（mkdocs.yml）

```yaml
site_name: KOIKI-FW v0.5.0
theme:
  name: material

nav:
  - 概要: index.md
  - KOIKI-FW 機能設計・構成ガイド: design_kkfw_0.5.0.md
```

### 依存関係

- **MkDocs**: 静的サイトジェネレータ（^1.6.1）
- **MkDocs Material**: モダンなUIテーマ（^9.6.14）

## 📝 ドキュメント編集

1. `docs/` ディレクトリ内のMarkdownファイルを編集
2. `poetry run mkdocs serve` でプレビュー確認
3. 変更をGitにコミット・プッシュ
4. GitHub Actionsまたは手動で `mkdocs gh-deploy` を実行

## 🎯 KOIKI-FWの特徴

KOIKI-FW v0.5.0は以下の特徴を持つエンタープライズ向けフレームワークです：

- **モダン技術スタック**: FastAPI, SQLAlchemy (Async), Pydantic, Redis, Celery
- **関心事の分離**: API層、サービス層、リポジトリ層の明確な分離
- **非同期処理**: 高パフォーマンスな非同期処理対応
- **型安全性**: Pydantic と型ヒントによる開発効率と安全性
- **セキュリティ**: JWT認証, RBAC, レートリミット等の基本機能
- **監視・ロギング**: 構造化ログ, 監査ログ, Prometheus連携
- **CI/CD**: GitHub Actionsによる自動テスト・品質チェック

## 📞 サポート

- **作成者**: Shuichi Kataoka
- **メール**: shu01k9@gmail.com
- **ライセンス**: エンタープライズ向けフレームワーク

---

> このドキュメントサイトは、エンタープライズ向けWebアプリケーション開発の実践的なガイドとして継続的に更新されています。
