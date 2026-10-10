# 応用データ分析演習 教材データ

長崎大学「応用データ分析演習」（全14回）の演習ノートで使用するデータ一式です。
受講生は Google Colab 上でノートを開き、冒頭の `DATA_DIR` からこれらの CSV を
読み込みます。手元にダウンロードする必要はありません。

## 収録データ

| ファイル | 内容 | 規模 | 原データのライセンス |
|---|---|---|---|
| `airbnb_tokyo.csv` | 東京の Airbnb 掲載の部屋の条件と1泊の料金 | 32,361行 × 16列 | CC BY 4.0（Inside Airbnb） |
| `ames_housing.csv` | 米国エイムズ市の住宅の条件と売買価格 | 2,930行 × 80列 | 文献引用（De Cock 2011） |
| `bike_day.csv` | シェアサイクルの日別利用台数と気象条件 | 731行 × 16列 | UCI（文献引用を要求） |
| `bike_hour.csv` | 同、時間別 | 17,379行 × 17列 | UCI（文献引用を要求） |
| `gapminder.csv` | 国・年ごとの平均寿命、人口、一人当たりGDP | 1,704行 × 8列 | CC-BY（Gapminder Foundation） |
| `heart.csv` | 心臓病診断の臨床指標と診断結果 | 303行 × 14列 | UCI（文献引用を要求） |
| `olivetti_faces.csv.gz` | 40人 × 10枚の顔画像（64×64画素の明るさ、gzip 圧縮） | 400行 × 4,097列 | AT&T Laboratories Cambridge（クレジット表記、scikit-learn が配布） |
| `movielens_genre_decade.csv` | 映画ジャンル × 公開年代のクロス集計 | 10行 × 9列 | 派生集計（下記参照） |
| `penguins.csv` | ペンギン3種の体格測定値 | 344行 × 7列 | CC-0 |
| `rat_eye.csv` | ラットの目の遺伝子発現量（TRIM32 と200遺伝子） | 120行 × 202列 | 文献引用（Scheetz 2006、NCBI GEO） |
| `rat_eye_full.csv.gz` | 同、全プローブ（gzip 圧縮） | 120行 × 31,100列 | 文献引用（Scheetz 2006、NCBI GEO） |
| `rat_eye_genes.csv` | プローブと遺伝子の名前の対応（GPL1355） | 31,099行 × 3列 | NCBI GEO（制限なし） |

各ファイルの詳しい出典・引用文献・加工内容は、同じディレクトリの
`<名前>_SOURCE.txt` に記載しています。

## 出典と引用

再利用する場合は、以下の引用要件に従ってください。

- **Inside Airbnb: Tokyo**（`airbnb_tokyo.csv`）
  Inside Airbnb, "Tokyo, Kantō, Japan"（2026-06-30 取得）— CC BY 4.0。
  <http://insideairbnb.com/>　教材用の16列に絞り、ホスト・物件を特定できる列は外した。

- **Ames Housing**（`ames_housing.csv`）
  De Cock, D. (2011). *Ames, Iowa: Alternative to the Boston Housing Data as an End of
  Semester Regression Project*. Journal of Statistics Education, 19(3).
  <https://jse.amstat.org/v19n3/decock/AmesHousing.txt>

- **Bike Sharing**（`bike_day.csv`, `bike_hour.csv`）
  Fanaee-T, H. and Gama, J. (2013). *Event labeling combining ensemble detectors
  and background knowledge*. Progress in Artificial Intelligence.
  <https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset>

- **Heart Disease**（`heart.csv`）
  Detrano, R. et al. / UCI Machine Learning Repository (Cleveland).
  <https://archive.ics.uci.edu/dataset/45/heart+disease>
  `processed.cleveland.data` を整形。`target` は 1=心臓病あり(num>0)、0=なし。

- **Gapminder**（`gapminder.csv`）
  Gapminder Foundation、CC-BY。plotly/datasets 経由で取得。
  <https://raw.githubusercontent.com/plotly/datasets/master/gapminder_with_codes.csv>

- **Palmer Penguins**（`penguins.csv`）
  Horst, A. M., Hill, A. P., and Gorman, K. B. (2020). *palmerpenguins: Palmer
  Archipelago (Antarctica) penguin data*. R package version 0.1.0.
  doi:10.5281/zenodo.3960218 — CC-0。元データは Dr. Kristen Gorman および
  Palmer Station Antarctica LTER による収集。

- **ラットの目の遺伝子発現**（`rat_eye.csv`）
  Scheetz, T. E. et al. (2006). Regulation of gene expression in the mammalian
  eye and its relevance to eye disease. *PNAS* 103(39): 14429–14434。
  NCBI GEO GSE5680 <https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5680>
  から、TRIM32 と分散の大きい200遺伝子に絞った（`tools/make_data/rat_eye.py`）。
  `rat_eye_full.csv.gz` は全プローブ、`rat_eye_genes.csv` は GPL1355 の注釈表から作った
  プローブと遺伝子の名前の対応（`tools/make_data/rat_eye_full.py`）。

- **Olivetti の顔画像**（`olivetti_faces.csv.gz`）
  AT&T Laboratories Cambridge が1992〜1994年に撮影した The Database of Faces
  <https://cam-orl.co.uk/facedatabase.html>。scikit-learn の `fetch_olivetti_faces`
  から、1枚を1行（4,096画素の明るさ0〜1）にし、人の番号の列 `person` を付けた
  （`tools/make_data/olivetti_faces.py`）。

- **MovieLens 由来の集計表**（`movielens_genre_decade.csv`）
  F. M. Harper and J. A. Konstan (2015). *The MovieLens Datasets: History and
  Context*. ACM TiiS. <https://grouplens.org/datasets/movielens/>

  **再配布についての注記。** このファイルは ml-latest-small の `movies.csv` から
  ジャンル欄と公開年を数え上げた 10ジャンル × 9年代のカウント表であり、評価値・
  ユーザー情報・個別作品行といった MovieLens の生データは一切含みません。
  GroupLens は生データの公開再配布を許可していない（"We typically do not permit
  public redistribution."）ため、`ml-latest-small` 本体はここに置かず、この集計表
  のみを配布しています。生データが必要な場合は GroupLens から直接入手してください。

## ライセンス

本リポジトリの成果物（整形済み CSV、集計表、`*_SOURCE.txt`、この README）は
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) で提供します。全文は
`LICENSE` を参照してください。

ただしこれは整形・集計・記述という本リポジトリ自身の寄与に対するライセンスであり、
収録した原データにはそれぞれ固有の条件があります。上記「出典と引用」の各項目を
必ず確認してください。
