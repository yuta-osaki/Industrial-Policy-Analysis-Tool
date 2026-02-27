# 準備中

# このページは、「産業政策分析ツール」のオンライン・アペンディクスです。

本マニュアルは、差の差の手法を用いて産業政策の効果を探索的に分析する「産業政策評価ツール」を提供しています。ツールの詳細は、RIETI PDPをご確認ください。
「産業政策評価ツール」の使用には、Rの実行環境が必要です。あらかじめご準備ください。

「Industrial-Policy-Analysis-Tool.zip」ファイルをダウンロードして、作業環境下で解凍してください。分析用コード、データ格納フォルダ、出力フォルダ、が格納されています。
本分析ツールは、３つのRコード（01_prepare.R、02_analysis.R、03_robustness）から構成されています。番号順に使用してください。
<img width="874*0.5" height="501*0.5" alt="image" src="https://github.com/user-attachments/assets/79fdf51c-6f4f-4e2f-9c9d-bb5b7a14f2d1" />

作成した分析ツールの詳細については、「簡易的な産業政策評価ツールの作成」をご覧ください。
[RIETI PDP（後日公表予定）]()
<!-- [html版](https://yutaaa0811.github.io/Industrial-Policy-Analysis-Tool/) -->

# 必要データの準備

kikatsu_rawdataのフォルダには、経済産業省企業活動基本調査の調査票情報（個票データ）を格納してください。
treated_listには、処置群企業（政策介入を受けた企業）のリストを格納してください。
dataフォルダには、地図データと産業名リストが格納されています（利用者の作業不要）。
<img width="868" height="957" alt="image" src="https://github.com/user-attachments/assets/bb572faa-d336-4e61-a4dc-11f6e43a8110" />


# 使用するファイル

## [01_prepare.R](https://github.com/yutaaa0811/Industrial-Policy-Analysis-Tool/blob/main/01_prepare.R)

××のcsv形式の調査票情報をパネルデータ化することができます。デフォルトでは、1995年から2023年のデータが必要です。

パネルデータは、merged_key.csvというファイル名で出力されます。

## [02_analysis.R](https://github.com/yutaaa0811/Industrial-Policy-Analysis-Tool/blob/main/02_analysis.R)

対象となる産業政策に関して差の差分析を行うことができます（本文の分析）。その際、「merged_key.csv」、「企業リスト.xlsx」、「industry_name.csv」を参照するため、参照先に格納されていることを確認してください。

## [03_robustness.R](https://github.com/yutaaa0811/Industrial-Policy-Analysis-Tool/blob/main/03_robustness.R)

分析結果の頑健性を確認する分析を行うことができます（Appendixの分析）。その際、「merged_key.csv」、「企業リスト.xlsx」、「industry_name.csv」を参照するため、参照先に格納されていることを確認してください。

## その他の提供ファイル

分析で用いる産業分類の一覧として、industry_name.csvを使用します。

サンプル用の分析データとして、●●の対象となった企業のリストを提供します（企業リスト.xlsx）。

## 利用者が個別に準備するファイル

「公的統計の二次的利用サービス」に関する[独立行政法人統計センター](https://www.nstac.go.jp/)のページを熟読の上、ご自身で申請して××の調査票情報を用意してください。調査票情報の扱いには十分に注意して下さい。

分析対象としたい政策の介入群の企業のリストをxlsx形式でご準備ください。

# 引用

本分析ツールを利用する際は、以下を引用してください。

# 免責事項

本分析ツールを利用して得られた分析結果に対して、作成者は一切の責任を負いません。
