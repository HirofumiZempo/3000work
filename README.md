# UMIN000061709 公開データ / Public Dataset

## 研究概要 / Study Overview

本リポジトリは、臨床試験登録番号 **UMIN000061709** に対応する研究の公開データセットです。  
This repository contains the public dataset associated with the clinical trial registered as **UMIN000061709**.

8週間のウォーキング介入が循環血中 small RNA（miRNA）発現プロファイルに与える影響を調べた前後比較研究のデータを収録しています。  
This is a pre-post intervention study examining the effects of an 8-week walking program on circulating small RNA (miRNA) expression profiles.

---

## 参加者 / Participants

- 参加者数：7名（JW1〜JW7）  
- Number of participants: 7 (labeled JW1–JW7)

---

## データファイル一覧 / Data Files

| ファイル名 | 内容 | 期間 | 備考 |
|---|---|---|---|
| `1_Steps_Pre.txt` | ベースライン期の日別歩数 | 7日間 | |
| `2_Steps_8wk.txt` | 介入期の日別歩数 | 最大56日間（8週間）| 一部欠損あり |
| `3_MVPA_Pre.txt` | ベースライン期の日別 MVPA | 7日間 | 単位：分/日 |
| `4_MVPA_8wk.txt` | 介入期の日別 MVPA | 最大56日間（8週間）| 単位：分/日、一部欠損あり |
| `5_readCounts_miRNAmature_sense.txt` | 成熟型 miRNA リードカウント（センス鎖）| 介入前後（Pre/Post）| 1,205 miRNA エントリ |
| `6_readCounts_smallRNA_Stats.xlsx` | small RNA シーケンシング統計 | 介入前後（Pre/Post）| Excel 形式 |

### ファイル詳細 / File Details

#### `1_Steps_Pre.txt` / `2_Steps_8wk.txt`（歩数データ / Step Count Data）

- 形式：タブ区切りテキスト
- 列：`Days`（日）、`JW1`〜`JW7`（各参加者の日別歩数）
- ベースライン平均歩数（7日間）は参加者により約 4,880〜7,569 歩/日

#### `3_MVPA_Pre.txt` / `4_MVPA_8wk.txt`（MVPA データ / MVPA Data）

- 形式：タブ区切りテキスト
- 列：`day`（日）、`JW1`〜`JW7`（各参加者の日別 MVPA、単位：分）
- MVPA（Moderate-to-Vigorous Physical Activity）：中〜高強度身体活動時間

#### `5_readCounts_miRNAmature_sense.txt`（miRNA リードカウント / miRNA Read Counts）

- 形式：タブ区切りテキスト（スペース区切り）
- 行：各 miRNA（hsa-let-7 ファミリーほか計 1,205 エントリ）
- 列：`miRNA`、`JW1Post`、`JW1Pre`、`JW2Post`、`JW2Pre`、…、`JW7Post`、`JW7Pre`
- `Pre`：介入前、`Post`：8週間介入後の血液サンプルから得られたリードカウント

#### `6_readCounts_smallRNA_Stats.xlsx`（シーケンシング統計 / Sequencing Statistics）

- 形式：Microsoft Excel
- small RNA シーケンシングの品質・マッピング統計情報を含む

---

## 研究デザイン / Study Design

```
ベースライン測定          8週間ウォーキング介入          介入後測定
（7日間）                （56日間）                    （血液採取）
Pre 歩数・MVPA  ────────────────────────────────→  Post 血中 miRNA
Pre 血液採取    →  日別歩数・MVPA モニタリング   →  Post 血液採取
```

---

## 欠損値 / Missing Values

一部の参加者・日付において歩数および MVPA のデータが欠損しています（セルが空白）。  
Some step count and MVPA values are missing (empty cells) for certain participants and days.

---

## データ形式の注意 / Data Format Notes

- テキストファイルはタブ区切り（`.txt`）です。
- 一部の歩数データにコンマ付き数値（例：`5,239`）が含まれます。読み込み時に適宜処理してください。
- miRNA リードカウントファイルはスペース区切りです。

---

## ライセンス / License

本データは研究目的での利用を想定しています。利用にあたっては UMIN000061709 の試験登録情報および関連論文を参照し、適切に引用してください。  
This dataset is intended for research use. Please refer to the UMIN000061709 trial registration and associated publications and cite them appropriately.

---

## 関連情報 / Related Information

- UMIN 臨床試験登録：https://www.umin.ac.jp/ctr/  
- 試験登録番号：UMIN000061709
