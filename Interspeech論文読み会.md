# SONY柏木さん
## 会社紹介
- 量よりも高付加価値を狙う会社戦略
- aiboにも認識や学習技術が使われている
- 高い技術を醸成する仕組み
- R&Dからも、商品サービス企画部に異動したりすることもできる
- 社内募集制度での異動
- クリエイティビティとテクノロジーで世界を感動で満たす

## Interspeech2019について
- 音声処理に関する学会
- 今年はオーストリア、４日間
- 採択率49%
- 9つものワークショップ

# The USTC System for BC2019
## 小谷さん（東大齋藤研究室D1）
- 声質変換
- TTSもしたい

## 論文概要
- 中国語TTSのタスクが一番良かったシステムを紹介

## Blizzard Challenge 2019
- ExpressiveなTTSを作れ！というタスク
- ブレスや抑揚の影響で変換前がそもそもExpressiveである

## FW
- BERTベースのフロントエンド

### 前処理
- 人手の処理のコスト
- どの語を強調するかも人手で設定
- Mel-cep, F0, V/UV
- HMM alignmentもした

## フロントエンド
- テキスト処理
  - アラビア数字など特殊な文字を変換
- 中国語のバウンダリー予測
- Focus wordsの予測も

### BERT
- 外部データとして小説とニュース記事の

## Duration Modeling
- 継続長をLogスケールで量子化してクロスエントロピーで学習
- Contextの入力：ピンインと四声
- Pre-trainedのマルチスピーカーモデルを1000時間以上使っていた

## Acoustic Modeling
- GANを使ってOversmoothingを回避している

## Vocoding
- 多人数話者でWavenet vocoder
- 16kHzと24kHzのWavenetをConcatした
- 位相はノイズで埋めてGriffin-Lim的なことをしているらしい

## まとめ
- BC2019
  - BERT-based
  - Autoregressive
  - GAN-based multi-task acoustic model
  - Wavenet-based neural vocoder
- まるで本人のような声が出ていて感動
