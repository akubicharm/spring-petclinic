## Postgresql を使う場合

application.properties に `spring.profiles.active=postgres` を追加。
スキーマ構成済みのDBの場合には、application-postgres.propertiesの
`spring.sql.init.mode=always` を `spring.sql.init.mode=never` に変更

OpenShiftにPostgresqlをデプロイするときに指定したユーザに権限があることを確認。
権限は `\du` で各院できる。
権限がない場合には `ALTER ROLE petclinic WITH Useruser;` などで、権限を付与する。