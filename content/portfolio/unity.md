+++
categories = ["unity", "multi"]
coders = ["0fk0", "inadai1783"]
github = ["https://github.com/0fk0/ox_game"]
date = 2023-09-13T13:00:00+09:00
description = "友人と共同で開発しました"
image = "/images/portfolio/ox_game_play.png"
title = "オンライン対戦可能なOXゲーム"
type = "post"
[[tech]]
logo = "/logos/unity.svg"
name = "Unity"
url = "https://unity.com/ja"
[[tech]]
logo = "/logos/photon.svg"
name = "PUN2"
url = "https://www.photonengine.com/ja-jp"
+++
## ルール
通常の三目並べと同様  

△注意△  
マッチングが完了するまでOXを置かないでください。途中入退室に対応していません。

## 仕様
- GUI  
    - ボード(3x3)  
    - 石(ox)
- 通信  
    - 交代  
    = 相手の番の時は動けない
    - 相手の処理の反映  
- 勝利条件  
    - 縦横斜め三つ揃えば勝ち
    - 勝敗が決定したときにどのラインで決着したか・どちらが勝利したかを表示

- プラットフォーム  
    - PC(Windows)

## プレイ画面
![play](/images/portfolio/ox_game_play.png)
![wait](/images/portfolio/ox_game_wait.png)

## 使用技術
- C#
- Unity
- PUN2(Photon Unity Network 2)

## 苦労した点
- Unityは少しさわったことがあったものの、raycastというマウスからレーザーが出てその先で当たり判定をつけるという処理は初めてで難しかった。
- オンラインで動作するゲームは初めて作ったのでプレイヤーの動ける状態の管理やプレイヤー間の処理の同期を行うことが初めてで難しかった。