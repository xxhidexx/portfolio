# ポートフォリオサイト

就職活動用のポートフォリオサイトです。Astro + Tailwind CSS で構築された高速で SEO に優れた静的サイトです。

## 🚀 特徴

- **高速**: Astroの静的サイト生成により、高速なページ読み込みを実現
- **レスポンシブ**: モバイルからデスクトップまで最適化されたデザイン
- **SEO最適化**: メタタグによる検索エンジン最適化
- **モダンなUI**: Tailwind CSSによる美しく一貫性のあるデザイン
- **条件付き表示**: GitHubリンクやデモサイトがある場合のみボタンを表示

## 📋 ページ構成

- **ホーム** (`/`): ヒーローセクション、開発実績、スキル紹介
- **開発実績** (`/works`): 開発プロジェクトの詳細一覧
- **プロフィール** (`/about`): 詳細な自己紹介、経歴（※現在非表示）
- **お問い合わせ** (`/contact`): コンタクトフォームと連絡先情報

## 🛠️ 技術スタック

- **フレームワーク**: [Astro](https://astro.build/) v5.9.0
- **スタイリング**: [Tailwind CSS](https://tailwindcss.com/) v4.1.8
- **デプロイ**: [Vercel](https://vercel.com/)
- **言語**: TypeScript, HTML, CSS

## 🚀 開発・デプロイ

### 前提条件

- Node.js 18以上
- npm

### ローカル開発

```bash
# 依存関係のインストール
npm install

# 開発サーバーの起動
npm run dev

# ブラウザで http://localhost:4321 にアクセス
```

### ビルド

```bash
# 本番用ビルド
npm run build

# ビルド結果のプレビュー
npm run preview
```

### Vercelへのデプロイ

1. GitHubリポジトリにコードをプッシュ
2. Vercelアカウントでリポジトリを連携
3. `vercel.json`設定により自動的にデプロイが開始されます

## 📁 プロジェクト構造

```
tasty-telescope/
├── public/                 # 静的ファイル（画像など）
├── src/
│   ├── components/         # 再利用可能なコンポーネント
│   │   ├── Header.astro   # ナビゲーションヘッダー
│   │   ├── Hero.astro     # ヒーローセクション
│   │   ├── Skills.astro   # スキル表示
│   │   ├── Works.astro    # 開発実績紹介
│   │   └── Footer.astro   # フッター
│   ├── layouts/           # ページレイアウト
│   │   └── Layout.astro   # 基本レイアウト
│   ├── pages/             # ページファイル
│   │   ├── index.astro    # トップページ
│   │   ├── works.astro    # 開発実績一覧
│   │   ├── about.astro    # プロフィールページ（非表示）
│   │   └── contact.astro  # お問い合わせページ
│   └── styles/            # スタイルファイル
│       └── global.css     # グローバルスタイル
├── astro.config.mjs       # Astro設定
├── vercel.json           # Vercel設定
└── package.json          # 依存関係とスクリプト
```

## 🎨 デザイン特徴

- **条件付きボタン表示**: GitHubリンクやデモサイトのURLが設定されている場合のみボタンを表示
- **レスポンシブレイアウト**: モバイルファーストでデザインされたUI
- **統一されたスタイル**: 主要実績とその他実績で一貫性のあるデザイン
- **アクセシブル**: 適切なaria-labelとキーボードナビゲーション

## 📝 カスタマイズ

### 個人情報の更新

以下のファイルで個人情報を更新してください：

- `src/components/Hero.astro` - 名前、自己紹介
- `src/components/Skills.astro` - スキル情報
- `src/components/Works.astro` - 開発実績情報
- `src/pages/works.astro` - 詳細な開発実績一覧
- `src/pages/contact.astro` - 連絡先情報

### 開発実績の追加

`src/components/Works.astro`と`src/pages/works.astro`のworksデータ配列に新しい項目を追加：

```javascript
{
  id: 5,
  title: "新しいプロジェクト",
  description: "簡単な説明",
  longDescription: "詳細な説明", // works.astroのみ
  technologies: ["React", "TypeScript"],
  github: "https://github.com/username/repo", // 空文字列の場合はボタン非表示
  url: "https://demo-site.com", // 空文字列の場合はボタン非表示
  featured: true // Works.astroで主要実績として表示するか
}
```

### 画像の追加

`public/`ディレクトリに画像を配置し、コンポーネントでパスを指定：

```astro
<img src="/your-image.jpg" alt="説明" />
```

## 🔧 主な機能

- **動的ボタン表示**: githubやurl属性が空でない場合のみボタンを表示
- **レスポンシブグリッド**: デバイスサイズに応じて最適なレイアウト
- **SEO対応**: 適切なメタタグとタイトル設定
- **フォーム処理**: お問い合わせフォームの実装

## 📄 ライセンス

このプロジェクトはMITライセンスの下で公開されています。

## 🚀 Astro コマンド

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | 依存関係をインストール                            |
| `npm run dev`             | ローカル開発サーバーを localhost:4321 で起動      |
| `npm run build`           | 本番用サイトを ./dist/ にビルド                   |
| `npm run preview`         | ビルド結果をローカルでプレビュー                  |
| `npm run astro ...`       | `astro add`, `astro check` などのCLIコマンドを実行 |

## 📚 参考リンク

- [Astro公式ドキュメント](https://docs.astro.build)
- [Tailwind CSS公式サイト](https://tailwindcss.com/)
- [Vercelデプロイガイド](https://vercel.com/docs)

```sh
npm create astro@latest -- --template minimal
```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/minimal)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/minimal)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/minimal/devcontainer.json)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).
