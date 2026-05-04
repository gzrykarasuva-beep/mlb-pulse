# MLB Pulse — セットアップ手順

## フォルダ構成
```
mlb-pulse/
├── vercel.json        ← Vercel設定
├── api/
│   ├── scores.js      ← 試合スコア取得API
│   └── players.js     ← 選手成績取得API
└── public/
    └── index.html     ← フロントエンド
```

## Vercelへのデプロイ手順

### 1. GitHubにアップロード
1. github.com で新しいリポジトリを作成（名前例: `mlb-pulse`）
2. このフォルダの中身を全部アップロード
   - `vercel.json`
   - `api/scores.js`
   - `api/players.js`
   - `public/index.html`

### 2. Vercelと連携
1. https://vercel.com にアクセス（GitHubアカウントでログイン）
2. "Add New Project" をクリック
3. 作成したGitHubリポジトリを選択
4. "Deploy" をクリック

### 3. 完了
数分後に `https://mlb-pulse-xxx.vercel.app` のようなURLが発行されます。
そのURLにアクセスするだけでリアルタイムデータが自動取得されます。

## データ更新タイミング
- ページを開いたとき: 自動取得
- 5分ごと: 自動更新
- 「更新」ボタン: 手動で即時取得

## 費用
- Vercel無料プラン: 月100GBの帯域、関数実行10万回まで無料
- MLB Stats API: 完全無料・APIキー不要
- 個人利用では費用ゼロです
