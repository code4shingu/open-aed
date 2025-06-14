# Code for Shingu - AEDデータ公開リポジトリ

このリポジトリは、福岡県新宮町の公共施設や民間施設に設置されている **AED（自動体外式除細動器）** の設置場所データを収集・整形し、再利用可能な形式で公開するプロジェクトです。

## 📦 利用可能なデータ

- `data/raw/*.csv`: AED設置箇所一覧 元データ

## API

- AED設置箇所一覧 元データ:  https://code4shingu.github.io/open-aed/raw/20240823aed.csv
- AED設置箇所一覧 加工データ: https://code4shingu.github.io/open-aed/processed/aed.csv

## Usage

```ts
import { CSV } from "https://js.sabae.cc/CSV.js";

const data = await CSV.fetchJSON("https://code4shingu.github.io/open-aed/processed/aed.csv");

console.log(data);
// [
//   {
//     "都道府県コード又は市区町村コード": "403458",
//     NO: "0000000001",
//     "都道府県名": "福岡県",
//     "市区町村名": "新宮町",
//     "名称": "新宮町役場",
//     "名称_カナ": "シングウマチヤクバ",
//     "住所": "福岡県糟屋郡新宮町緑ケ浜一丁目1-1",
//     "緯度": "33.715311",
//     "経度": "130.446596",
//     "設置位置": "１階ロビー",
//     "電話番号": "(092)962-0231",
//     "団体名": "新宮町",
//     "利用可能曜日": "月火水木金",
//     "開始時間": "08:30",
//     "終了時間": "17:00",
//     "利用可能日時特記事項": "祝・休日、12/29～1/3を除く",
//     "小児対応設備の有無": "有"
//   },
```

## 🔗 出典

元データは [BODIK（オープンデータポータル）](https://data.bodik.jp/organization/403458) にて公開されているものを利用しています。

## ⚖️ データライセンス

本データは [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.ja) ライセンスのもとで公開されています。