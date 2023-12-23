+++
categories = ["self", "web-dev"]
coders = []
github = ["https://github.com/0fk0/Uroto"]
date = 2022-02-14T13:00:00+09:00
description = "自分用のアーティストサイト"
Image = "/images/portfolio/Uroto_top.png"
title = "Artist Site"
type = "post"
[[tech]]
logo = "/logos/github.svg"
name = "GitHub"
url = "https://docs.github.com/ja/pages/getting-started-with-github-pages/about-github-pages"
+++

## Contents
※画像は削除しました
- News  
×身バレ防止×
- Biography   
×身バレ防止×
- Discography  
×身バレ防止×
- Link  
×身バレ防止×

## 仕様
- SPA
- 画面下のボタンクリックで画面を再描画
- 緑色の枠内で縦スクロールができる
- レスポンシブ対応

## 使用技術
- HTML
- Sass
- JavaScript
- React

## 課題
- Reactを初めて扱ったということもありpropsとstateを理解しきれていなかった。  
(チュートリアルを進めながら制作した)
- 理解があまいことから、再描画するコンポーネントを分離しきれず、現在はボタンを含めて再レンダリングしてしまっている。これはコンポーネントを分離させることが可能

## 苦労した点
- 当時はhtmlのaタグでしか画面の切り替えを知らなかったのでDOMの概念からより深く理解する必要があり難しいと感じた。
- ボタンクリックでどのボタンがクリックされたかを取得し、再レンダリングされるコンポーネントのJSXを出力するという部分が難しいと感じたことを覚えている。
