+++
categories = ["web-dev", "multi"]
coders = ["0fk0", "Akira3085", "429uuuu"]
github = ["https://github.com/0fk0/hamamatsu-1"]
date = 2023-09-13T13:00:00+09:00
description = "株式会社Relicインターンシップ"
image = "/images/portfolio/relic.png"
title = "ペーパードライバーを救いたい"
type = "post"
+++
## サービス概要  
#### (課題)    
大学生や都内の方などペーパードライバーが多く、ペーパーになればなるほど車にのりたくても乗れなくなってしまう
#### (解決策)  
講習所の自動車講習と気軽に車が借りれるカーシェアのサービスを一気に使えるサービスを作る  
→このサービスは仲介を担うサービスである

## 使用方法
1. ペーパードライバー診断を行う  
→診断に応じて表示するレンタル可能な車種が変更される(5人乗り以上か否か)
2. 車の選択を行う
3. 車レンタルの予約を行う
4. それに応じて車の講習日時を指定し予約を行う
5. 当日借りた車で講習を受けることができる！

## ワイヤーフレーム
![wireframe](/images/portfolio/relic_wireframe.png)

## ER図
![ER](/images/portfolio/relic_er.png)

## 使用技術
- php
- Sass
- UIkit
- Laravel

## 課題
- 5日間という短い間に開発の上流から下流まで行ったので実際の予約部分がモックだけとなり実装しきれなかった。  
→拡張できるならデータベース部分で実装可能な部分を実装したい
- フロントのデザインが雑になってしまったことでUXを低下させている可能性がある。  
→アンケートの部分など導入から使ってもらえるようにするにはUIも大切だと思う

## 苦労した点
- 共同開発ということで上流での意見の食い違いなどもおこり議論が難しく苦労した。
- 共同開発においてDockerのエラーに悩まされた班員がいたので使い慣れない環境という部分の難しさも味わった。