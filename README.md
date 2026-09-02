# React GitHub Pages Template

AIエージェントがWebアプリケーションを開発する際に使い回すための、モダンで高品質なReactプロジェクトテンプレートです。

## 技術スタック

- **React 18+** (TypeScript)
- **Vite** (最新安定版)
- **TailwindCSS v3+**
- **React Router v6+** (GitHub Pages SPA対応)
- **Zustand** (状態管理)
- **lucide-react** (アイコン)
- **Vitest + React Testing Library** (テスト)

## セットアップ手順

### 1. リポジトリのクローン

```bash
git clone https://github.com/<your-username>/react-github-pages-template.git
cd react-github-pages-template
```

### 2. 依存パッケージのインストール

```bash
npm install
```

### 3. 開発サーバーの起動

```bash
npm run dev
```

ブラウザで `http://localhost:5173` が自動的に開きます。

## 開発コマンド一覧

| コマンド | 説明 |
|---------|------|
| `npm run dev` | 開発サーバーを起動（HMR対応） |
| `npm run build` | プロダクションビルドを生成 |
| `npm run preview` | ビルド成果物をプレビュー |
| `npm run lint` | ESLint でコードを検証 |
| `npm run lint:fix` | ESLint で自動修正 |
| `npm run format` | Prettier でコードをフォーマット |
| `npm run type-check` | TypeScript の型チェック |
| `npm run test` | テストを実行 |
| `npm run test:ui` | テストをUIモードで実行 |

## ディレクトリ構成

```
src/
├── components/
│   ├── atoms/        # 最小単位のコンポーネント（Button, Input 等）
│   ├── molecules/    # atoms の組み合わせ（SearchBar 等）
│   ├── organisms/    # molecules の組み合わせ（Header 等）
│   ├── templates/    # ページレイアウト（DefaultLayout 等）
│   └── pages/        # ルーティング対象のページ（HomePage 等）
├── hooks/            # カスタムフック
├── stores/           # Zustand ストア
├── utils/            # ユーティリティ関数
├── types/            # 型定義
├── styles/           # グローバルCSS
├── constants/        # 定数定義
├── test/             # テストセットアップ
├── App.tsx           # ルートコンポーネント
├── main.tsx          # エントリーポイント
└── vite-env.d.ts     # Vite 型定義
```

## GitHub Pages へのデプロイ

### 自動デプロイ（推奨）

1. GitHub リポジトリの **Settings** > **Pages** > **Source** を **"GitHub Actions"** に設定する
2. `vite.config.ts` の `BASE_PATH` をリポジトリ名に合わせて変更する
   ```ts
   const BASE_PATH = process.env.VITE_BASE_PATH || '/your-repo-name/';
   ```
3. `main` ブランチに push すると自動的にデプロイされる

### 手動デプロイ

```bash
npm run build
```

`dist/` ディレクトリに生成された成果物をデプロイしてください。

## 関連ドキュメント

- [BLUEPRINT.md](./BLUEPRINT.md) - プロジェクト仕様書
- [.agents/AGENTS.md](./.agents/AGENTS.md) - AIエージェント行動指示書

## ライセンス

MIT
