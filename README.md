# 🌤️ WeatherNow - リアルタイム天気予報ダッシュボード

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![OpenWeatherMap](https://img.shields.io/badge/OpenWeatherMap-API-orange?style=for-the-badge)

## 🌟 概要

OpenWeatherMap APIを使用したリアルタイム天気予報ダッシュボード。美しいグラスモーフィズムデザインと天気に応じたアニメーション効果で、天気情報を視覚的に表現します。

### ✨ デモ

[🔗 ライブデモはこちら](https://se0831.github.io/weather-dashboard/)

*※ デモを動作させるには、OpenWeatherMap APIキーの設定が必要です*

### 📸 スクリーンショット

<details>
<summary>クリックして表示</summary>

#### 晴天時
![Clear Weather](https://via.placeholder.com/800x500/667eea/ffffff?text=Clear+Weather+View)

#### 雨天時（アニメーション付き）
![Rainy Weather](https://via.placeholder.com/800x500/3a7bd5/ffffff?text=Rainy+Weather+Animation)

#### モバイル表示
![Mobile View](https://via.placeholder.com/400x800/667eea/ffffff?text=Mobile+Responsive)

</details>

## 🎯 主な機能

### 🌡️ 天気情報
- **現在の天気** - リアルタイムの気温、体感温度、天気状況
- **詳細情報** - 湿度、風速、気圧、視程、UV指数
- **5日間予報** - 最高/最低気温と天気アイコン
- **時間別予報** - 24時間の詳細予報

### 🎨 ビジュアル機能
- **動的背景** - 天気に応じて変化するグラデーション
- **天気アニメーション** - 雨、雪、雲のリアルなアニメーション
- **グラスモーフィズム** - 透明感のあるモダンなUI
- **絵文字アイコン** - 直感的な天気表現

### 🔧 便利機能
- **都市検索** - 世界中の都市の天気を検索
- **現在地取得** - GPS位置情報から天気を取得
- **お気に入り都市** - 複数都市の天気を一覧表示
- **単位切り替え** - 摂氏/華氏の切り替え
- **表示設定** - 12/24時間表示、風速単位の変更
- **データ保存** - 設定をLocalStorageに保存

## 🛠️ 使用技術

| カテゴリ | 技術 | 用途 |
|---------|------|------|
| **API** | OpenWeatherMap API | 天気データ取得 |
| **フロントエンド** | HTML5, CSS3, JavaScript | UI構築 |
| **デザイン** | Glassmorphism | モダンなUI表現 |
| **アニメーション** | CSS Animations | 天気エフェクト |
| **アイコン** | Font Awesome | UIアイコン |
| **位置情報** | Geolocation API | 現在地取得 |

## 🚀 セットアップ

### 1. APIキーの取得

1. [OpenWeatherMap](https://openweathermap.org/)でアカウント作成（無料）
2. [API Keys](https://home.openweathermap.org/api_keys)からAPIキーを取得
3. APIキーをコピー（32文字の英数字）

### 2. プロジェクトのセットアップ

```bash
# リポジトリをクローン
git clone https://github.com/SE0831/weather-dashboard.git
cd weather-dashboard

# index.htmlをコピーしてローカル版を作成
cp index.html index-local.html
```

### 3. APIキーの設定

`index-local.html`の398行目付近を編集：

```javascript
// 変更前
const API_KEY = 'YOUR_API_KEY_HERE';

// 変更後（あなたのAPIキーに置き換え）
const API_KEY = 'あなたのAPIキー';
```

### 4. ブラウザで開く

```bash
# Macの場合
open index-local.html

# Windowsの場合
start index-local.html
```

## 📖 使い方ガイド

### 都市を検索
1. 検索ボックスに都市名を入力（英語）
2. Enterキーまたは検索ボタンをクリック
3. 例：Tokyo, New York, London, Paris

### 現在地の天気
1. 位置情報ボタン（📍）をクリック
2. ブラウザの位置情報許可を承認
3. 自動的に現在地の天気を表示

### 設定のカスタマイズ
- **温度単位** - °C/°Fボタンで切り替え
- **アニメーション** - 設定パネルでON/OFF
- **時刻表示** - 12時間/24時間表示を選択
- **風速単位** - m/s ⇔ km/hを切り替え

## 🎨 カスタマイズ

### お気に入り都市の変更

```javascript
// 402行目付近
let favoriteCities = ['Tokyo', 'New York', 'London', 'Paris'];
// お好みの都市に変更可能
```

### 背景色の変更

```css
/* 各天気の背景グラデーション */
.weather-bg.clear {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

## 📊 API制限

OpenWeatherMap無料プラン：
- **呼び出し回数**: 60回/分
- **1日の上限**: 1,000回/日
- **データ更新**: 10分ごと
- **利用可能期間**: 無期限

## 🔒 セキュリティ

- APIキーは公開リポジトリにコミットしない
- ローカル版（`index-local.html`）は`.gitignore`に追加
- 本番環境では環境変数やバックエンドサーバーの使用を推奨

## 📁 ファイル構成

```
weather-dashboard/
├── index.html           # メインファイル（APIキー要設定）
├── index-local.html     # ローカル動作用（gitignore）
├── .gitignore          # Git除外設定
├── README.md           # このファイル
└── LICENSE            # MITライセンス
```

## 🚧 今後の改善予定

- [ ] 天気マップの追加
- [ ] 週間予報の拡張（7日間）
- [ ] 雨雲レーダー
- [ ] 気象警報・注意報
- [ ] 花粉情報
- [ ] 紫外線情報の詳細
- [ ] PWA対応
- [ ] 多言語対応
- [ ] ウィジェット機能
- [ ] 天気の共有機能

## 🤝 貢献

プルリクエストは大歓迎です！

1. フォーク
2. フィーチャーブランチ作成 (`git checkout -b feature/AmazingFeature`)
3. コミット (`git commit -m 'Add some AmazingFeature'`)
4. プッシュ (`git push origin feature/AmazingFeature`)
5. プルリクエスト作成

## 📝 ライセンス

このプロジェクトはMITライセンスの下で公開されています。詳細は[LICENSE](LICENSE)ファイルをご覧ください。

## 👨‍💻 作者

**SE0831**

- GitHub: [@SE0831](https://github.com/SE0831)
- ポートフォリオ: [その他のプロジェクト](https://github.com/SE0831?tab=repositories)

## 🙏 謝辞

- [OpenWeatherMap](https://openweathermap.org/) - 天気データAPI
- [Font Awesome](https://fontawesome.com/) - アイコンセット
- [Google Fonts](https://fonts.google.com/) - Webフォント

## 💡 関連プロジェクト

他のポートフォリオ作品もご覧ください：

- [💰 家計簿アプリ](https://github.com/SE0831/expense-tracker-app)
- [📋 タスク管理アプリ](https://github.com/SE0831/task-management-app)
- [📊 売上分析ダッシュボード](https://github.com/SE0831/sales-analytics-dashboard)
- [📩 お問い合わせフォーム自動通知システム](https://github.com/SE0831/google-forms-chatwork-notifier)

## ⭐ サポート

このプロジェクトが役に立ったら、⭐スターをお願いします！

---

*最終更新: 2024年8月*
