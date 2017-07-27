# 自然言語処理と深層学習の勉強会
- リカレントニューラルネットワーク(RNN)入門 #1

---
# About me
- @Masashi_Ueda
- 画像認識エンジニア
    - 丁度[CVPR 2017 速報](https://www.slideshare.net/cvpaperchallenge/cvpr-2017-78294211)眺めてます

+++?image=https://cdn.img-conv.gamerch.com/img.gamerch.com/imascg-slstage-wiki/1460213259001.jpg&size=contain

+++
# About me
- @Masashi_Ueda
- 画像認識エンジニア
- 本業: 346P |
    - 明日から福岡

---
# アチーブメント(前)
1. FFNNの気持ちを知る
1. NNの言葉を覚える
1. RNNの気持ちを知る
1. LSTMの気持ちを知る

+++?image=http://www.asimovinstitute.org/wp-content/uploads/2016/09/neuralnetworks.png&size=contain

---
# Level 1
![ffnn](http://www.asimovinstitute.org/wp-content/uploads/2016/09/ff.png)
Note:
<!--
- 今日の晩御飯を決める例 // 受けなさそうだけど
    - inputはラーメン/カレーライスが食べたいときそれぞれ1
    - output層は重みの大きい方を出力
    - 重みという言葉をどこかで言う
    - peprceptronの場合
        - ラーメンの重みが高い -> どっちも食べたいときはラーメン
        - 実際は両方食べたいけど8:2かなみたいなこともあり
            - 出力は10:0しか起こらないので少し誤差が発生する
            - 誤差を元に重みを更新する
    - MLPの場合
        - 増えた層は金額・栄養バランスとしておく
        - カレー食べたいけどお金ないからラーメンといった判断ができるようになる
    - 同じ(ような)インターフェースを持つものを組み合わせて高度なことができるようになった！！
-->
+++
# Level 2
- forward propagation
    - 入力を順に伝播させて出力を得る
    - 活性化関数: セルの出力形を決める関数
Note:
<!-- 入力層/隠れ層/出力層/(結合)重み -->

+++
# Level 3
- optimization: ネットワーク構造の最適化
    - コスト関数: NNの出力と正解の「違い」を測る物差し
    - 勾配降下法: コスト関数が減る方向に重みを更新する
        - 参考: [最適化と学習アルゴリズム](http://www.r.dl.itc.u-tokyo.ac.jp/~nakagawa/SML1/opt-algorithm1.pdf)
        - 参考*: [勾配降下法の最適化アルゴリズムを概観する](http://postd.cc/optimizing-gradient-descent/)
    - back propagation: コスト関数が減る方向を効率的に求める計算法

+++
# Level 4(RNN)
![rnn](http://www.asimovinstitute.org/wp-content/uploads/2016/09/rnn.png)
Note:
<!--
- 今日の晩御飯を決める例
    - 系列を扱えるようになった
        - 昨日食べたものが反映される
    - 注意
        - input層が複雑に
            - 1回分のラーメン/カレーライスが食べたいかどうかを1つの入力セルで表す
        - 途中の隠れ層も複数の評価を一つのセルで行う
-->

+++
![rnn-time](https://4.bp.blogspot.com/-4sNWGgBFLkE/WKcLzxWRa9I/AAAAAAAAiGQ/sqV16vvhGH09_QyZK5sIPJ8UcEyhekp5ACLcB/s1600/OldR%251C%251CNN.png)
Note:
<!--
- 1本(?)を時間展開
- 昨日の判断と今日食べたいものを入力としていることを言いたい
-->

+++
# Level 5(LSTM)
![lstm](http://www.asimovinstitute.org/wp-content/uploads/2016/09/lstm.png)
Note:
<!--
- 記憶用のセルを導入
    - LSTMセルは複数のセルが集まったもの
- 素朴なRNNだと10系列分くらいしか記憶できない
    - 購買消失
-->

---
# アチーブメント(前)
1. FFNNの気持ちを知る
1. NNの言葉を覚える
1. RNNの気持ちを知る
1. LSTMの気持ちを知る


---
# まとめ

+++
# なんかかけ
