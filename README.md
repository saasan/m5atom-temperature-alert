# m5atom-temperature-alert

M5Stack ATOM Lite で気温を監視し、閾値を超えたら Slack へアラートメッセージを送信

## 必要なもの

- M5Stack ATOM Lite
- M5Stack用温湿度気圧センサユニット Ver. 4 (ENV IV)

## 機能

- 10秒ごとに温度を測定し、閾値を超えたら Slack へアラートメッセージを送信 (測定間隔は変更可)
- 1時間1回記録した温度をグラフ化し設定時刻に Slack へ送信

## secrets.h の作成

secrets.h という名前でファイルを作成し
Wi-Fi の SSID とパスフレーズ、Slack のエンドポイントのパスを
書き込んでおく必要があります。

    // Wi-FiのSSID
    const char* WIFI_SSID = "Wi-FiのSSID";
    // Wi-Fiのパスフレーズ
    const char* WIFI_PASSPHRASE = "Wi-Fiのパスフレーズ";
    // Incoming Webhook URLのパス
    const char* WEBHOOK_PATH = "/services/xxxxx/xxxxx/xxxxx";
