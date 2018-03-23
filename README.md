# DeepLearningでアップサンプリングする
オーディオ界隈はオカルトっぽく見えていたので、今までどうしようと思っていたのですが、簡単な感じで結果がでました  

世の中、音のアップサンプリングや音質がよくなるような細工に本当に余念がないのですが、ディープラーニングでも簡単に対応することは可能です。  


## High Resolution
ハイレゾは96kHz/24bitという高いサンプリング数と、高い解像度を誇ります。  

通常、YouTubeでは44kHz/16bitで音楽が再生されるので、及ばないのですが、15kHz/16bitの音源を44kHz/16bitに引き上げてみます。  

<p align="center">
  <img width="450px" src="https://user-images.githubusercontent.com/4949982/37853846-c2b195ca-2f2b-11e8-9af8-db0cd526b819.png">
</p>
<div align="center"> 図1. 今回やりたいこと </div>

## 今回使用したネットワーク
幾つかやり方にはコツがあって、実は音の16bit値をfloatに変換したのでは、うまく行きません  

そのため、16bitをバイナリ（２進数）表記に変換して、音のある波形の16サンプルを切り出します。 
16サンプルから、44kHzで本来存在していただろう、音の波形を補完します。  

ネットワークでは、双方向のLSTMのネットワークを用いました。  

<p align="center">
  <img width="450px" src="https://user-images.githubusercontent.com/4949982/37854467-625d8c76-2f2e-11e8-8089-103202987a82.png">
</p>
<div align="center"> 図2. 全体のデータの流れ　</div>
## 実験

## 結果（誤差評価）

## 結果（聞いてみる）

## まとめ


## オカルト
- [1] [mp3音源を“アップサンプリング”で高音質化できるか試してみた](https://kakakumag.com/pc-smartphone/?id=9459)
