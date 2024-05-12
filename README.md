# clean_corpus
日本語特化LLMのための日本語コーパスクリーニング

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

## URLフィルタリング
* ブラックリスト([リンク](https://dsi.ut-capitole.fr/blacklists/))
* 

## dedup
* Minhash：高速化したい
* Exact


## 参考にするもの
* LLM-jp cprpus([リンク](https://gitlab.llm-jp.nii.ac.jp/datasets/llm-jp-corpus-v2))
* RefinedWeb コーパスと、その模倣であるFinedWeb([リンク](https://github.com/huggingface/datatrove/tree/main/src/datatrove/pipeline/filters)、
[論文](https://arxiv.org/abs/2306.01116)、[記事](https://qiita.com/kernelian/items/1ea84c8f7da43fb5bb6b))
* Swallowコーパス([発表スライド](https://speakerdeck.com/aya_se/data-centric-ai-swallow-corpus-56e2869a-f9bd-46cb-b030-1012235c37f7)、[NLP2024の論文](https://www.anlp.jp/proceedings/annual_meeting/2024/pdf_dir/A6-1.pdf)、[論文](https://arxiv.org/abs/2404.17790))
* hatakeyamaさんのコード([リンク](https://note.com/kan_hatakeyama/n/nf5b102271f82#1506e7dd-5be2-4e9a-8724-ca9d87dde60a))
* Gopher([論文](https://note.com/kan_hatakeyama/n/nf5b102271f82#1506e7dd-5be2-4e9a-8724-ca9d87dde60a](https://arxiv.org/abs/2112.11446)))
* [note](https://www.notion.so/matsuolab-geniac/7edfb573e2de4949b8ea2993449eb1ae)
