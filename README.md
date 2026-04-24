# 8028-design-adjustment

8028 Private Salon の **営業時間管理** 画面の静的デザイン（HTML 単体）を Netlify に載せるためのリポジトリです。

- **本番 URL（例）**: `https://8028-design-adjustment.netlify.app/`
- **ビルド**: なし（ルートの `index.html` をそのまま公開）

## Netlify での Git 連携（既存サイトへ接続）

1. [Netlify](https://app.netlify.com) → プロジェクト **8028-design-adjustment** → **Project configuration** → **Build & deploy**
2. **Continuous deployment** で **Link repository** を選択
3. このリポジトリ（GitHub: `AFtakeuma/8028-design-adjustment` など）を選ぶ
4. ビルド設定はリポジトリの `netlify.toml` が使われます（**Publish directory**: `.`、**Build command**: 未指定で可）
5. **Deploy site** で初回デプロイ

手動デプロイ（Agent Runners / ドラッグ）から切り替えたあとは、**main**（または既定ブランチ）への push で自動デプロイされます。

## ローカル確認

`index.html` は `file://` では表示できない場合があるため、HTTP で開いてください。

```bash
cd 8028-design-adjustment
npx --yes serve .
# → http://localhost:3000/ など
```

## 更新手順

1. Figma Make 等から HTML を再エクスポートしたら、このリポジトリの **`index.html` を差し替え**
2. `git commit` して `git push`
3. Netlify が自動デプロイ

## 関連

- 報酬ダッシュボード本体（別リポ）: `8028-rewards-dashboard`
