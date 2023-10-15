+++
categories = ["web-dev", "self"]
coders = []
github = ["https://github.com/0fk0/Music-Alert"]
date = 2021-12-20T13:00:00+09:00
description = "音楽を用いて習慣化"
Image = "/images/portfolio/MusicAlert.png"
title = "Music Alert"
type = "post"
[[tech]]
logo = "/logos/netlify.svg"
name = "Netlify"
url = "https://www.netlify.com/"
+++


# Music Alert
Link: [app](/webapp/MusicAlert/home.html) (本ポートフォリオ内に静的サイトとして配置)
![top](/images/portfolio/MusicAlert_top.png)
![content](/images/portfolio/MusicAlert_content.png)


## 使用方法
1. YouTubeのリンク又はデバイス内の音声ファイルを指定する
2. 何分後指定か/時間指定かを選択し、時間を指定
3. startボタンを押し、アラームを起動(alertウィンドウで確認)
4. ブラウザを開けたまま他の作業を行う

## 仕様
- setTimeout関数という非同期関数を用いて指定時間後に非同期でアラームが起動するようにする
- アラームの内容は別ウィンドウでYouTubeのリンクを開くか、webのオーディオAPIから音声を鳴らす

## 使用技術
- HTML
- Sass(元はCSS)
- UIkit
- JavaScript 

## 課題
- 時間の処理をdate型の差分を取得したりしている関係でまだ24をまたぐときだったりにバグが残っていると思われる
- 初めてjavascriptをさわった機会ということもあり、コードの可読性が悪いのでリファクタリングする必要がある。  
→リファクタリングを別ブランチで行ったがその結果今まで動いていた機能が動かなかったのでリファクタリングしたコードはマージしていない

## 苦労した点
- 初めて個人開発をしたアプリケーションだったこともあり、非同期関数の仕様などドキュメントを見ながら苦労してコーディングした記憶がある
