スケジュールをExcelで出力できるアプリを作る

## ■Usersテーブル（ユーザー）

|Column|Type|Options|
| -------- | -------- | -------- |
|name|string|null: false|
|password|string|null: false, unique: true, index: true|
### Association
- has_many :lists

***

## ■listsテーブル(スケジュールの予定）エクセルで出力する情報

|Column|Type|Options|
| -------- | -------- | -------- |
|day|string|null: false|
|list|string|null: false|
|user_id|references|null: false, foreign_key: true|
### Association
- belongs_to :user
