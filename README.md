# clean_corpus
日本語特化LLMのためのコーパスクリーニング

[進捗スライド](https://docs.google.com/presentation/d/13dZ441Xn6dv7MKsed0zbcSHNyBHGoJH_NuQZdbB5x14/edit#slide=id.g2cf042e6629_0_164)

現状はCommonCrawlからのクリーニング、WARC形式から。

## 粗めの日本語判別
* lang=japanese以外になっているものをフィルター

## テキスト抽出
* trafulaturaの用いて抽出(warc形式からtrafilaturaを用いるのが、品質面での重要なポイント)

## 日本語判定
* 厳密な日本語フィルタリング

## 品質フィルタリング
* 文字のなさ
* 繰り返し表現削除
* ヘッダー、フッター
　　*　MLベース 


## dedup
* Minhash
* Exact


## 参考にするもの
* LLM-jp cprpus([リンク](https://gitlab.llm-jp.nii.ac.jp/datasets/llm-jp-corpus-v2))
* RefinedWeb コーパスと、その模倣であるFinedWeb([リンク](https://github.com/huggingface/datatrove/tree/main/src/datatrove/pipeline/filters))

* Swallowコーパス
* hatakeyamaさんのコード([リンク](https://note.com/kan_hatakeyama/n/nf5b102271f82#1506e7dd-5be2-4e9a-8724-ca9d87dde60a))
