# gcal-slack-sync

GoogleカレンダーとSlackのステータスをなんか良い感じにsyncするやつ

## 概要

Googleカレンダーの予定から「休暇」や「リモート」を拾って、Slackのステータスを動的に更新したい。
通知も止まるように出来たら尚良い。

### 参考

- <https://liginc.co.jp/584979>
- <https://zenn.dev/nokonpt/articles/gas-calendar-status-slack>

## 設計と実装

- プログラムは予定を持つGoogleカレンダーと同一のGASで稼働する。
- GoogleカレンダーとSlackアカウントは1対1とする。
- デプロイはGASにコピペする。
  - パラメータの一覧はこのREADMEに後述するが、静的に埋め込む。

## 必要なパラメータ

- calendarID
- SlackAPI
