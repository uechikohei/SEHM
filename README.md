# SEHM
`docker-compose build`
@rails6.0(ruby3.0.0) では solidus gem が動作しない
@rails 5.2(ruby2.6.6) に変更してください。
build時、`--no-cache`の付与を忘れずに

(
  NoMethodError: undefined method arityとなる。
  引数に関するエラーが出ており、アソシエーションが組めていないと考える。
)

`docker-compose run app bash`

`bundle install`

- rails new(mysql選択、バンドルスキップ、テストスキップ)
`rails new . -d mysql --skip-bundle --slip-test`

- config/datebase.ymlでdocker-compose.yml内のmysqlコンテナを指定する
`host→db`
`password→root`

- solidus設定
`bundle exec rails g spree:install`
聞かれることには、Y→none→emailとパスワード6桁を入力→Yを選択


- localhost:3000/adminでオーナー画面
- localhost:3000でユーザー画面
`docker-compose up`
