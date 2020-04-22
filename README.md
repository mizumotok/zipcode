# 郵便番号検索API
郵便番号から住所を返すAPI（JSON）

## API仕様

**GET** /api/***{code1}***/***{code2}***.json

### 処理概要
郵便番号７桁を指定すると、住所や全国地方公共団体コード（JIS X0401、X0402）等を返します。

### 例
```
/api/100/0001.json
```

### パラメータ
- code1: 郵便番号の上3桁
- code2: 郵便番号の下4桁

### レスポンス
```json
{
  "local_government_code":"13101",
  "zip_code":"1000001",
  "address":["東京都","千代田区","千代田"],
  "address_kana":["ﾄｳｷｮｳﾄ","ﾁﾖﾀﾞｸ","ﾁﾖﾀﾞ"]
}
```

## 元データ
[日本郵政の住所の郵便番号（CSV形式）- 読み仮名データの促音・拗音を小書きで表記しないもの](https://www.post.japanpost.jp/zipcode/dl/kogaki-zip.html)
