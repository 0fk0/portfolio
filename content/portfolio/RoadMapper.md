+++
categories = ["web-dev", "self"]
coders = []
github = ["https://github.com/0fk0/RoadMapper_front", "https://github.com/0fk0/RoadMapper_back"]
date = 2023-09-20T13:00:00+09:00
description = "最適な学習手順を提供"
Image = "/images/portfolio/roadmapper_top.png"
title = "Road Mapper"
type = "post"
[[tech]]
logo = "/logos/vercel.svg"
name = "Vercel(front)"
url = "https://vercel.com"
[[tech]]
logo = "/logos/render.svg"
name = "Render(back)"
url = "https://render.com/"
+++


# RoadMapper
Link: [app](https://road-mapper-front.vercel.app/)
![content](/images/portfolio/roadmapper_logo.png)
![top](/images/portfolio/roadmapper_top.png)
![content](/images/portfolio/roadmapper_content.png)


## フロントエンド仕様
### 機能
- レスポンシブ対応
- 入力欄全てを埋めたときのみ送信(HTTPリクエスト)
- フロー生成時間の待機アニメーション

![loading](/images/portfolio/roadmapper_loading.gif)

- フロー生成待機中は送信不可

## バックエンド仕様
### API
- (オリジン)/generateを叩くと以下gptResTypeのjson形式のHTTPレスポンスが返る
```typescript
export interface gptResType {
  word: string;
  topic: string;
  flow: flowPairType[];
}

export interface flowPairType {
  num: number;
  title: string;
  flow: string;
}
```
- flowPairType型はフロントから受け取った学習対象に対しての学習手順をChatGPTのプロンプトに入れ、応答を分割し格納した
- ChatGPTへの学習対象はDeepLで翻訳し、質問自体は英語で行う  
→英語での応答を全てDeepLで翻訳

## 使用技術
- TypeScript
- Next.js(React)
- Sass
- Nest.js  

(関連)
- dotenv
- vercel
- ChatGPT API
- DeepL API

## 課題
- APIを叩く待機時間が長い  

※初期生成時はバックエンドの初期起動も入るため1分半程待つ必要があります。二回目以降は約30秒程で生成されます。  
→バックエンドの初期起動はバックエンドのデプロイ先のRenderの仕様なのでアップグレードして解決するしかない
- 応答文の形式が定まらないことから分割が上手くいかない場合が生じる  
→質問文でより詳細に形式を指定等

## 苦労した点
- 今回はMVCモデルなどのフロントとバックをまとめて考えるやり方ではなく、フロントとバックを分離して開発したのでCORS対策なども含めて初めてのエラーなどが多く苦労した。
- Next.jsとNest.js自体初めてさわったものなので学習も含めて一週間程度で完成させるのが難しかった。
- 機能としてChatGPTのプロンプトから返されたメッセージを一定の字句かたまりごとに分離するというものがあるが、ChatGPTも毎回同じような形式で出してくれる訳ではないのでそこが難しいと思った。これは改善点でもある。