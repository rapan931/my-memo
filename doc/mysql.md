# MySql

## file出力

```sql
SELECT フィールド名 FROM テーブル名 INTO OUTFILE 'ファイル名';

` 例
SELECT * FROM tests INTO OUTFILE '/var/path/to/file.dmp';
```

`secure_file_priv` が設定されている場合は設定されているディレクトリ以外への出力はエラーになる
