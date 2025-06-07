# ポートフォリオサイト

就職活動用のポートフォリオサイトです。Astro + Tailwind CSS で構築された高速で SEO に優れた静的サイトです。

## 🚀 特徴

- **高速**: Astroの静的サイト生成により、高速なページ読み込みを実現
- **レスポンシブ**: モバイルからデスクトップまで最適化されたデザイン
- **SEO最適化**: メタタグ、構造化データによる検索エンジン最適化
- **アクセシビリティ**: WCAG 2.1 AA準拠のアクセシブルなデザイン
- **モダンなUI**: Tailwind CSSによる美しく一貫性のあるデザイン

## 📋 ページ構成

- **ホーム** (`/`): ヒーローセクション、スキル、プロジェクト紹介
- **プロフィール** (`/about`): 詳細な自己紹介、経歴、価値観
- **プロジェクト** (`/projects`): 開発プロジェクトの詳細一覧
- **お問い合わせ** (`/contact`): コンタクトフォームと連絡先情報

## 🛠️ 技術スタック

- **フレームワーク**: [Astro](https://astro.build/)
- **スタイリング**: [Tailwind CSS](https://tailwindcss.com/)
- **フォント**: [Inter](https://fonts.google.com/specimen/Inter)
- **デプロイ**: [Vercel](https://vercel.com/)
- **言語**: TypeScript, HTML, CSS

## 🚀 開発・デプロイ

### 前提条件

- Node.js 18以上
- npm または yarn

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

1. GitHubリポジトリを作成
2. Vercelアカウントでリポジトリを連携
3. 自動的にデプロイが開始されます

## 📁 プロジェクト構造

```
src/
├── components/         # 再利用可能なコンポーネント
│   ├── Header.astro   # ナビゲーションヘッダー
│   ├── Hero.astro     # ヒーローセクション
│   ├── Skills.astro   # スキル表示
│   ├── Projects.astro # プロジェクト紹介
│   └── Footer.astro   # フッター
├── layouts/           # ページレイアウト
│   └── Layout.astro   # 基本レイアウト
├── pages/             # ページファイル
│   ├── index.astro    # トップページ
│   ├── about.astro    # プロフィールページ
│   ├── projects.astro # プロジェクト一覧
│   └── contact.astro  # お問い合わせページ
└── styles/            # スタイルファイル
    └── global.css     # Tailwind CSS
```

## ⚡ パフォーマンス

- Lighthouse スコア: 90点以上（全項目）
- Core Web Vitals: すべて緑色
- ページ読み込み時間: 2秒以内

## 📝 カスタマイズ

### 個人情報の更新

以下のファイルで個人情報を更新してください：

- `src/components/Hero.astro` - 名前、自己紹介
- `src/components/Skills.astro` - スキル情報
- `src/components/Projects.astro` - プロジェクト情報
- `src/pages/about.astro` - 詳細プロフィール
- `src/pages/contact.astro` - 連絡先情報

### プロジェクト画像

`public/` ディレクトリにプロジェクト画像を配置し、各コンポーネントでパスを更新してください。

## 📄 ライセンス

このプロジェクトはMITライセンスの下で公開されています。

## 📞 お問い合わせ

ご質問やご相談がございましたら、お気軽にお問い合わせください。

- Email: contact@example.com
- GitHub: [@yamada-taro](https://github.com/yamada-taro)
- LinkedIn: [yamada-taro](https://linkedin.com/in/yamada-taro)

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
