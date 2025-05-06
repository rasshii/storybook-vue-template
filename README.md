# Storybook Vue テンプレート

## 概要

このプロジェクトは、Vue.jsとStorybookを使用したコンポーネント開発のためのテンプレートです。Storybookを使用することで、コンポーネントを独立して開発・テスト・ドキュメント化することができます。

## 主な機能

- Vue.js 3.x対応
- Storybook 7.x対応
- TypeScriptサポート
- コンポーネントの独立した開発環境
- インタラクティブなドキュメント
- レスポンシブデザインのテスト
- アクセシビリティテスト

## 必要条件

- Node.js 16.x以上
- npm 7.x以上

## セットアップ方法

1. リポジトリのクローン

```bash
git clone https://github.com/your-username/storybook-vue-template.git
cd storybook-vue-template
```

2. 依存関係のインストール

```bash
npm install
```

3. 開発サーバーの起動

```bash
npm run storybook
```

## 使用方法

### 新しいコンポーネントの作成

1. `src/components`ディレクトリに新しいコンポーネントを作成
2. `src/stories`ディレクトリに対応するストーリーファイルを作成
3. コンポーネントのストーリーを記述

### ストーリーの書き方

```typescript
import type { Meta, StoryObj } from '@storybook/vue3';
import YourComponent from '../components/YourComponent.vue';

const meta = {
  title: 'Components/YourComponent',
  component: YourComponent,
  tags: ['autodocs'],
} satisfies Meta<typeof YourComponent>;

export default meta;
type Story = StoryObj<typeof meta>;

export const Default: Story = {
  args: {
    // コンポーネントのプロパティ
  },
};
```

## プロジェクト構造

```
storybook-vue-template/
├── src/
│   ├── components/     # Vueコンポーネント
│   ├── stories/        # Storybookストーリー
│   └── assets/         # 静的アセット
├── .storybook/         # Storybook設定
├── package.json
└── README.md
```

## スクリプト

- `npm run storybook`: Storybook開発サーバーの起動
- `npm run build-storybook`: Storybookのビルド
- `npm run test`: テストの実行
- `npm run lint`: コードのリント

## 貢献方法

1. このリポジトリをフォーク
2. 新しいブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m 'Add some amazing feature'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. プルリクエストを作成

## ライセンス

MITライセンスの下で公開されています。詳細は[LICENSE](LICENSE)ファイルを参照してください。

## 作者

[あなたの名前]

## サポート

問題や質問がある場合は、GitHubのIssueを作成してください。
