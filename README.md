# community-template-lp

AIサロン向けの静的ランディングページです。トップページ、下層ページ、過去LPをHTML単体で管理しています。

## フォルダ構成

```text
.
├── index.html              # トップページ
├── contact.html            # お問い合わせ
├── privacy.html            # プライバシーポリシー
├── terms.html              # 利用規約
├── tokushoho.html          # 特定商取引法に基づく表記
├── assets/                 # トップページ共通画像
├── lp1/                    # 過去LP 1
├── lp2/                    # 過去LP 2
└── scripts/                # 補助スクリプト
```

## よく変更する箇所

- サービス名: `AIサロン`
- 月額料金: `2,980円`
- 入会ボタンの遷移先: `https://stripe.com/en-jp`
- お問い合わせリンク: `mailto:` の宛先
- FV画像: `assets/ai-salon-fv-man.png`
- 代表プロフィール画像: `assets/ai-salon-profile.png`
- イベント画像: `assets/event-dummy.svg`

## 運用メモ

- 画像は `assets/` に集約し、ファイル名は用途が分かる英数字のケバブケースを推奨します。
- `.wrangler/` や `.env` はローカル環境用のためGit管理に含めません。
- ページを追加する場合は、既存の下層ページのヘッダー・フッター構成をコピーして、サービス名やCTAの表記を揃えてください。
- 大きなデザイン改修を行う場合は、`index.html` 内のCSSが肥大化しやすいため、将来的に `assets/css/` への分離を検討してください。

## 確認コマンド

```bash
npm run sync-peatix:dry
```
