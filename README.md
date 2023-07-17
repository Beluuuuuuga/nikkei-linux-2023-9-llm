# 日経Linux2023年9月号LLM特集サポートページ
## 概要
2023年8月8日に日経BPから出版される**日経Linux2023年9月号**のLLM特集の「LLMをカスタマイズしてLinuxコマンドを覚えさせる」特集のサポートページです。 

## 学習コード
### 動作環境
- 学習コードはGoogleColaboratoryのA100で動作することを確認しています。
- 無料版のGoogleColaboratoryでは動作しませんのでご了承ください。
- 動作時のGoogleColaboratoryのランタイムは以下の通りです。
  - ランタイムのタイプ: Python
  - ハードウェアアクセラレータ： GPU
  - GPUのタイプ: A100
  - ランタイムの仕様: ハイメモリ
 
![image](https://github.com/Beluuuuuuga/nikkei-linux-2023-9-llm/assets/45144084/e8797903-9103-4711-94e8-fabe6cdf552a)

 
### 学習ノートブックの動作方法
- [notebook](https://github.com/Beluuuuuuga/nikkei-linux-2023-9-llm/blob/main/notebook/japanese_instruction_linux_command.ipynb)をダウンロードし、ご自身の環境でJupyterNotebookを用いてGPU環境で動作させるかGoogleDriveにアップロードしてGoogleColaboratoryにて動作させてください。
- GoogleColaboratoryで利用する際はランタイムの設定を動作環境で紹介した設定にして動作させてください。

## 学習データ
### 記事内での学習データの利用方法
- 169個のLinuxコマンドについて質問したデータセット**Japanese-Instruction-Linux-Command-169**を作成し、ファインチューニングを行っています。

### 利用方法
- **Japanese-Instruction-Linux-Command-169**は[HuggingFaceのページ](https://huggingface.co/datasets/Beluuuuuuga/Japanese-Instruction-Linux-Command-169)と[GitHubリポジトリ](https://github.com/Beluuuuuuga/nikkei-linux-2023-9-llm/blob/main/data/japanese-instruction_linux_command-169.json)に保存していますのでどちらからかご利用ください。
- PythonもしくはJupyterNotebook(GoogleColaboratory)でのHuggingFaceの場合の利用方法は以下の通りです。
```py
from datasets import load_dataset

dataset = load_dataset("Beluuuuuuga/Japanese-Instruction-Linux-Command-169")
```
- GitHubリポジトリから直接利用する場合は、ローカルにjapanese-instruction_linux_command-169.jsonをダウンロードし利用ください。

### ライセンス
- Japanese-Instruction-Linux-Command-169(japanese-instruction_linux_command-169.json)のデータは研究目的でのみ使用することを意図し、ライセンスを付与しています。このデータセットはCC BY NC 4.0（非商用利用のみ許可）であり、このデータセットを使って学習したモデルは非営利目的以外では使用しないでください。
- Japanese-Instruction-Linux-Command-169(japanese-instruction_linux_command-169.json)データを除く部分についてはApache License 2.0が付与されています。

### 注意事項
- OpenAI社は、ChatGPTの出力結果を利用して「競合となるLLMを開発すること」を禁じていますが、本記事ではあくまでLLMのファインチューニングを試す目的で利用します。
- 詳細はOpenAI社の[Terms of use](https://openai.com/policies/terms-of-use)の2. Usage Requirementsの(c) Restrictionsの(iii)を参照ください。

## 参考文献
記事内で参照した参考文献です。記事内では `[3]` と記載があれば、以下の `[3]` の参考文献を参照しています。

- [1] https://arxiv.org/abs/2205.11916
- [2] https://arxiv.org/abs/2005.14165
- [3] https://platform.openai.com/docs/guides/fine-tuning
- [4] https://openai.com/pricing
- [5] https://arxiv.org/abs/2109.01652
- [6] https://arxiv.org/abs/2106.09685
- [7] https://arxiv.org/abs/2303.15647
- [8] https://rinna.co.jp/news/2023/05/20230507.html
- [9] https://www.cyberagent.co.jp/news/detail/id=28817
- [10] https://huggingface.co/datasets/databricks/databricks-dolly-15k
- [11] https://huggingface.co/datasets/tatsu-lab/alpaca
- [12] https://github.com/kunishou/databricks-dolly-15k-ja
- [13] https://huggingface.co/datasets/Beluuuuuuga/Japanese-Instruction-Linux-Command-169


