jlacd-conv [![](https://img.shields.io/badge/python-3.7+-blue.svg)](https://docs.python.org/3.7/)
=============================================================
日本図書館協会選定図書総目録CD-ROMのデータ変換ツール

概要
-----
- 日本図書館協会選定図書総目録のデータを使いやすい形に変換
- 抽出したデータはLine-delimited JSON形式で保存
- [図書選定事業](http://www.jla.or.jp/activities/sentei/tabid/207/Default.aspx)は2016年3月に終了しています

依存パッケージのインストール
----
```json
pipenv install
```

コマンドライン
----

- 各CD-ROM内の"JBISCS"ファイルをコピーする
- 複数ファイルをまとめて処理する場合は、プログラムを直接修正する

```bash
pipenv run python jlacd-conv.py > jlacd.jsonl
```

処理済みデータのダウンロード
----

現在準備中です

- 処理済みデータにはISBNおよび選定年が含まれます（書誌情報は含みません）
- ISBNの付与されていない選定図書は除外されています
- このデータは「単なる事実」の集合であり著作権の対象外です
- 処理に用いた元情報は以下の通りです

  | タイトル       | ISBN          | 期間                                          |
  |----------------|---------------|-----------------------------------------------|
  | 選定図書目録59 | 9784820408109 | 2003年1月～2007年12月                         |
  | 選定図書目録64 | 9784820413103 | 2008年1月～2012年12月                         |
  | 選定図書目録67 | 9784820416043 | 2011年1月～2016年3月<br>1996年～2010年の児童図書 |

- 1996年～2016年3月の20年間のデータを統合しています
