# 応用データ分析演習 教材データ

長崎大学「応用データ分析演習」（全14回）の演習ノートで使用するデータ一式です。
受講生は Google Colab 上でノートを開き、冒頭の `DATA_DIR` からこれらの CSV を
読み込みます。手元にダウンロードする必要はありません。

## 収録データ

| ファイル | 内容 | 規模 | 原データのライセンス |
|---|---|---|---|
| `airbnb_tokyo.csv` | 東京の Airbnb 掲載の部屋の条件と1泊の料金 | 32,361行 × 16列 | CC BY 4.0（Inside Airbnb） |
| `ames_housing.csv` | 米国エイムズ市の住宅の条件と売買価格 | 2,930行 × 80列 | 文献引用（De Cock 2011） |
| `auto_mpg.csv` | 1970〜1982年の車の性能（燃費・排気量・馬力・重さなど） | 398行 × 9列 | UCI（CC BY 4.0、文献引用） |
| `bike_day.csv` | シェアサイクルの日別利用台数と気象条件 | 731行 × 16列 | UCI（文献引用を要求） |
| `bike_hour.csv` | 同、時間別 | 17,379行 × 17列 | UCI（文献引用を要求） |
| `gapminder.csv` | 国・年ごとの平均寿命、人口、一人当たりGDP | 1,704行 × 8列 | CC-BY（Gapminder Foundation） |
| `heart.csv` | 心臓病診断の臨床指標と診断結果 | 303行 × 14列 | UCI（文献引用を要求） |
| `olivetti_faces.csv.gz` | 40人 × 10枚の顔画像（64×64画素の明るさ、gzip 圧縮） | 400行 × 4,097列 | AT&T Laboratories Cambridge（クレジット表記、scikit-learn が配布） |
| `nsw.csv` | 職業訓練の実験（くじ引きで訓練の有無を決めた445人の収入） | 445行 × 10列 | 文献引用（LaLonde 1986、Dehejia & Wahba 1999） |
| `tecator.csv` | ひき肉240個の近赤外の吸収スペクトル（850〜1048nm、100本）と、化学分析で測った水分・脂肪・たんぱく質の割合 | 240行 × 103列 | パブリックドメイン（Tecator の許可文を添えて再配布可） |
| `sms_spam.csv` | 携帯電話の SMS の本文と、迷惑（spam）か普通（ham）かのラベル（英語） | 5,574行 × 2列 | CC BY 4.0（UCI、文献引用） |
| `online_shoppers.csv` | ネットショップの訪問ごとの、見たページの数と時間・直帰率・離脱率・ページ価値などと、購入したか | 12,330行 × 18列 | CC BY 4.0（UCI、文献引用） |
| `gaia_nearby.csv` | 太陽から50パーセク以内の恒星の、視差・見かけの明るさ（G等級）・色（BP−RP）（Gaia DR3） | 27,860行 × 4列 | CC BY-SA 3.0 IGO（ESA、クレジット表記と文献引用） |
| `penguins.csv` | 南極のパーマー基地近くの3つの島で測った3種のペンギンの、くちばしの長さと深さ・ひれの長さ・体重・性別など（palmerpenguins） | 344行 × 8列 | CC0 |
| `world_climate.json` | 世界の67都市の、2015〜2024年の毎日の平均気温（°C）と降水量（mm）。Open-Meteo の API が返した JSON をそのまま都市ごとに入れたもの | 67都市 × 3,653日 | CC BY 4.0（Open-Meteo、クレジット表記） |
| `openflights_routes.dat`・`openflights_airports.dat` | 世界の航空路線（出発・到着の空港、2014年6月まで）と空港（名前・都市・国・緯度・経度・時間帯）。OpenFlights のファイルをそのまま | 67,663行・7,698行 | ODbL（OpenFlights、クレジット表記。公開する派生物も自由なライセンスで） |
| `upworthy_exploratory.csv.gz` | ニュースサイト Upworthy の見出しのA/Bテスト（2013〜2015年）。1行が1つのテストの中の1つの案で、見出し・画像の番号・表示の数・クリックの数など。Upworthy Research Archive の exploratory の表を gzip で縮めただけ | 22,666行 × 17列（4,873件のテスト） | CC BY 4.0（Cornell University、論文の引用） |
| `sdss_galaxies.csv` | 銀河の5色の明るさ（等級）と、分光で測った赤方偏移（SDSS DR18） | 14,983行 × 9列 | SDSS（公開、クレジット表記と文献引用） |
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

- **National Supported Work Demonstration**（`nsw.csv`）
  LaLonde, R. J. (1986). *Evaluating the Econometric Evaluations of Training Programs with
  Experimental Data*. The American Economic Review, 76(4), 604–620.
  Dehejia, R. H., and Wahba, S. (1999). *Causal Effects in Nonexperimental Studies*.
  Journal of the American Statistical Association, 94(448), 1053–1062.
  <https://users.nber.org/~rdehejia/data/>

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

- **自動車の性能**（`auto_mpg.csv`）
  Quinlan, R. (1993). Combining Instance-Based and Model-Based Learning. *ICML*。
  UCI Machine Learning Repository の Auto MPG <https://archive.ics.uci.edu/dataset/9/auto+mpg>
  を、seaborn の配布する形（`mpg`）のまま書き出した（`tools/make_data/auto_mpg.py`）。
  単位は米国の単位のまま。単位の換算と欠測6台の除外はノートで行う。

- **SDSS の銀河**（`sdss_galaxies.csv`）
  Sloan Digital Sky Survey, Data Release 18（Almeida et al. 2023, ApJS 267, 44）。
  <https://skyserver.sdss.org/dr18/>　SkyServer の SQL 検索で、空の一角の銀河の5色の等級と赤方偏移を取った
  （`tools/make_data/sdss_galaxies.py`）。

- **Tecator**（`tecator.csv`）
  Tecator AB が Tecator Infratec Food and Feed Analyzer で測った、ひき肉の近赤外の吸収スペクトル。
  StatLib で配布され、OpenML（データ番号505）が再配布している <https://www.openml.org/d/505>。
  許可文：パブリックドメイン。許可文を添えれば再配布できる。結果を発表するときは、装置と会社の名前（Tecator）を書く。
  OpenML が足した主成分の22列を外し、吸収の列の名前を波長（nm）にした（`tools/make_data/tecator.py`）。

- **SMS Spam Collection**（`sms_spam.csv`）
  Almeida, Gómez Hidalgo & Yamakami (2011), DocEng'11。UCI Machine Learning Repository
  <https://archive.ics.uci.edu/dataset/228/sms+spam+collection>（CC BY 4.0）。
  元のタブ区切りのファイルを、列 `label`・`text` の CSV にした（`tools/make_data/sms_spam.py`）。

- **Online Shoppers Purchasing Intention**（`online_shoppers.csv`）
  Sakar, Polat, Katircioglu & Kastro (2019), Neural Computing and Applications 31。UCI Machine Learning Repository
  <https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset>（CC BY 4.0）。
  `ucimlrepo` で取ってきた列と並びのまま CSV にした（`tools/make_data/online_shoppers.py`）。第7回のノートは `fetch_ucirepo(id=468)` で直接読む。

- **Gaia DR3 の近くの恒星**（`gaia_nearby.csv`）
  Gaia Collaboration, Vallenari et al. (2023), Astronomy & Astrophysics 674, A1。ESA の Gaia アーカイブ
  <https://gea.esac.esa.int/archive/>（CC BY-SA 3.0 IGO）。ESA と DPAC へのクレジットは `gaia_nearby_SOURCE.txt`。
  視差20ミリ秒角より大きい（50パーセク以内）星を、測りの質の条件で絞って取った（`tools/make_data/gaia_nearby.py`、条件は SOURCE に）。

- **世界の航空路線**（`openflights_routes.dat`・`openflights_airports.dat`）
  OpenFlights <https://openflights.org/data>（Open Database License、個々の内容は Database Contents License）。
  GitHub の jpatokal/openflights の `data/routes.dat`・`data/airports.dat` を手を加えずに置いた（`tools/make_data/openflights.py`）。路線は2014年6月で更新が止まっている。

- **Upworthy Research Archive**（`upworthy_exploratory.csv.gz`）
  J. N. Matias, K. Munger, M. Aubin Le Quere and C. Ebersole (2021). *The Upworthy Research Archive,
  a time series of 32,487 experiments in U.S. media*. Scientific Data 8, 195.
  <https://doi.org/10.1038/s41597-021-00934-7>。OSF <https://osf.io/jd64p/>（CC BY 4.0）の
  exploratory の表を、中身に手を加えずに gzip で縮めて置いた（`tools/make_data/upworthy.py`）。

- **世界の都市の気候**（`world_climate.json`）
  Open-Meteo Historical Weather API <https://open-meteo.com/>（CC BY 4.0）。"Weather data by Open-Meteo.com"。
  元は ECMWF の再解析データ（ERA5 など、Copernicus Climate Change Service）。67都市の緯度・経度で2015〜2024年の毎日の値を頼み、返ってきた JSON を手を加えずに入れた（`tools/make_data/world_climate.py`）。

- **パーマーペンギン**（`penguins.csv`）
  Horst, A. M., Hill, A. P., & Gorman, K. B. (2020). palmerpenguins: Palmer Archipelago (Antarctica) penguin data. R package
  <https://allisonhorst.github.io/palmerpenguins/>（CC0）。元のデータは Gorman, Williams & Fraser (2014), PLoS ONE 9(3), e90081 と Palmer Station LTER。
  GitHub の公開リポジトリの `inst/extdata/penguins.csv` をそのまま置いた（`tools/make_data/penguins.py`）。

- **Olivetti の顔画像**（`olivetti_faces.csv.gz`）
  AT&T Laboratories Cambridge が1992〜1994年に撮影した The Database of Faces
  <https://cam-orl.co.uk/facedatabase.html>。scikit-learn の `fetch_olivetti_faces`
  から、1枚を1行（4,096画素の明るさ0〜1）にし、人の番号の列 `person` を付けた
  （`tools/make_data/olivetti_faces.py`）。

- **MovieLens**（第14回。ここには置かない）
  F. M. Harper and J. A. Konstan (2015). *The MovieLens Datasets: History and
  Context*. ACM TiiS. <https://grouplens.org/datasets/movielens/>

  GroupLens は生データの公開再配布を許可していない（"We typically do not permit
  public redistribution."）ため、ml-latest-small はこのリポジトリに置かない。
  第14回のノートが、GroupLens のページ
  （<https://files.grouplens.org/datasets/movielens/ml-latest-small.zip>）から
  取ってきて展開し、映画の一覧 `movies.csv` だけを使う。手元の写し
  （`ml-latest-small/`）は版管理せず、公開もしない（`.gitignore`、`tools/publish.sh`）。

## ライセンス

本リポジトリの成果物（整形済み CSV、集計表、`*_SOURCE.txt`、この README）は
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) で提供します。全文は
`LICENSE` を参照してください。

ただしこれは整形・集計・記述という本リポジトリ自身の寄与に対するライセンスであり、
収録した原データにはそれぞれ固有の条件があります。上記「出典と引用」の各項目を
必ず確認してください。
