# BW2 SHINY JOURNEY

ブラック2・ホワイト2の色違いリビングコレクションとOBS配信操作をまとめた独立Webアプリです。

## MVP範囲

- 19番道路（通常草むら）
- サンギ牧場（通常草むら）
- 3DS 1台／2台表示
- B2／W2個別ターゲット・遭遇数
- 捕獲記録と進化用途
- 場所別・全体進捗
- IndexedDB自動保存
- JSONバックアップ・復元
- BroadcastChannelによるOBS即時反映

## ファイル

- `index.html` 管理・操作画面
- `obs.html` OBSブラウザソース
- `app.js` データ・保存・連動
- `styles.css` 管理画面・OBSデザイン

OBSブラウザソースは `obs.html` を指定し、幅1920×1080を推奨します。

## データ分離

専用IndexedDB `bw2ShinyJourneyDB_v1` のみを使用します。SHINY HOME COLLECTIONのキー、DB、Supabaseには接続しません。

## MVPマスターデータ

19番道路とサンギ牧場の通常草むらのみを収録しています。出現率はSerebii Pokéarth、Veekun、Pokémon Databaseで照合した値を採用しています。揺れる草むら、波乗り、隠し穴などはMVPに含めません。
