# テーブル設計

## users テーブル
| Column             | Type   | Options                  |
| ------------------ | ------ | -------------------------|
| email              | string | null: false, unique true |
| nickname           | string | null: false              |
| encrypted_password | string | null: false              |

### Association
- has_many :memories

## memories テーブル
| Column             | Type      | Options                        |
| ------------------ | ----------| -------------------------------| 
| name               | string    | null: false                    |
| explanation        | text      | null: false                    |
| region_id          | integer   | null: false                    |
| user               | references| null: false, foreign_key: true |

### Association
- belongs_to :user
