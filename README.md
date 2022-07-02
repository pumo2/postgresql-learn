# postgresql-learn
以下の本を参考に学習を進める。
[SQL 第2版 ゼロからはじめるデータベース操作](https://www.amazon.co.jp/gp/product/B01HD5VWWO/ref=ppx_yo_dt_b_d_asin_title_o00?ie=UTF8&psc=1)

### VSCodeのSettingsからEncoding設定を変更する
1. `Command ＋ ,`でSeetingsを開く
2. Japanese (Shift JIS)に変更

または、
`.vscode`フォルダを作成し、
`settings.json`ファイルにEncoding設定を入れておく
```json
{

"files.encoding": "shiftjis",

}
```

# dockerで環境構築を行い、コンテナ上のPostgreデータベースにアクセス
```
docker-compose up -d
docker-compose exec db bash
psql -h 127.0.0.1 -p 5432 -U default_user -W default_db
```
