## 📌 環境構築

### 1. リポジトリをクローン
```sh
git clone https://github.com/your-username/skynote-fe.git
cd skynote-fe
```

### 2. 依存関係のインストール
```sh
npm install
# または
yarn install
```

### 3.環境変数の設定（必要なら）
.env ファイルを作成し、APIのURLを指定してください。
```sh
VITE_API_BASE_URL=http://localhost:5000/api
```

###　4. 開発サーバーの起動
```sh
npm run dev
# または
yarn dev
```

## 🛠 API との連携

- APIのエンドポイント（Flask）からデータを取得し、Vueで表示
- `.env` でAPIのURLを指定可能

## 🚀 デプロイ（予定）

- **ローカル開発**: `npm run dev`
- **本番環境**: Vercel / Netlify などを想定

## 📄 ライセンス

このプロジェクトは MIT ライセンスのもとで公開されています。

