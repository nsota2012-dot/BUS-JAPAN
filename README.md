# 🚌 バス運転ゲーム (Bus Driving Game)

実際の航空写真の上でバスを運転するブラウザゲームです。HTML 1ファイルだけで動きます。

## 特徴
- Google 航空画像の上を走る(Leaflet 使用)
- 場所検索(OpenStreetMap Nominatim)・現在地にバスを置ける
- 操作切替: タッチ版(スマホ / iPad)と キーボード版(PC)
- 車種: **ALLISON AT バス**(6速オート、D/N/R 表示)と **MT バス**(6速マニュアル、クラッチ・ストールあり)
- ディーゼル風エンジン音(Web Audio、回転数連動)

## 遊び方
`index.html` をブラウザで開く(要インターネット接続)。

| | タッチ版 | PC版 |
|---|---|---|
| アクセル / ブレーキ | ▲ / ■ | ↑ W / ↓ S |
| ハンドル | ◀ ▶ | ← → A D |
| 駐車ブレーキ | - | Space |
| AT シフト | R N D ボタン | Z=R X=N C=D (Q/E で1段ずつ) |
| MT シフト | ▼ ▲ ボタン + クラッチ | Q/E または 1〜6、Shift=クラッチ |
| エンジン始動/停止 | 🔑 | Enter |

## GitHub Pages で公開
1. このリポジトリを GitHub に push
2. Settings → Pages → Source: `Deploy from a branch` / Branch: `main` `/ (root)`
3. `https://<ユーザー名>.github.io/<リポジトリ名>/` で遊べます

## 注意
- 地図タイルは Google の非公式タイル URL を使用しています。個人利用・学習向けです。
  公開サービスとして運用する場合は Google Maps Platform(Map Tiles API)のキーを取得して差し替えてください。
- 場所検索は Nominatim の[利用ポリシー](https://operations.osmfoundation.org/policies/nominatim/)に従ってください。

## License
MIT

## 追加機能
- ウィンカー(左/右/ハザード、点滅音あり・曲がり終わると自動で消える)
- 3D視点(斜め追従カメラ)。🎥で「3D追従 / 3D左側面 / 真上 / 北固定」を切替
- 前ドア・後ドアを個別に開閉(停車中のみ。開いていると発進できません)
- マルチタッチ対応(ハンドル+アクセル+クラッチなど同時操作可)
