# ロボット聴覚オープンソフトウェアの（OSS）の何たるかを説いてみる

## 1. はじめに

はいどうも、アドベントカレンダー4日目を担当する3年の[yoshiki495](https://github.com/yoshiki495)です。

先日、HRIと京大が開発・公開しているHARK（Honda Research Institute Japan Audition for Robots with Kyoto University）というロボット聴覚のオープンソースソフトウェア（OSS）の講習会にお邪魔してきました。

ちなみにこのロボット聴覚という研究分野、日本初だとか。さすが京大と言わざるを得ません。

この記事ではHARKというロボット聴覚OSSを筆者の知識を織り混ぜながらできるだけわかりやすく説いていこうと思います。

## 2. ロボット聴覚とは

## 2. HARK の概要

HARKの主要機能と処理の流れは以下のようになっています。

![hark_overview](https://user-images.githubusercontent.com/68012132/204194793-9cbfe489-484b-4c65-a1ea-b996c067e3ce.jpeg)

簡単に説明すると、

1. 複数のマイクロホン（マイクロホンアレイ）を用いた音源収集
2. 音源の到来方向を推定（音源定位/Sound Source Localization）・音源を追跡（音源追跡/Sound Source Tracking）
3. 音源を分離抽出（音源分離/Sound Source Separation）
4. 音声を認識（音声認識/Automatic Speech Recognition）

といった感じです。

これらの主要機能含めさまざまな音に関するアルゴリズムをパッケージ化したソフトウェアこそがHARKであり、


### 参考
- https://www.jstage.jst.go.jp/article/itej/71/9/71_647/_pdf
- https://www.slideshare.net/DaichiKitamura/acoustic-modeling-in-audio-source-separation
