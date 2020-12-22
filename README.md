# テーブル設計

## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| nick_name| string | null: false |
|first_name| string | null: false |
|last_name | string | null: false |
|fname_kana| string | null: false |
|lname_kana| string | null :false |
| email    | string | null: false            |
| password | string | null: false            |
| profile  | text   | null: false            |
|occupation| text   | null: false            |
| position | text   | null: false            |




### Association
- has_many :item
- has_many :order
- 
  

## items テーブル

| Column     | Type   | Options     |
| ------     | ------ | ----------- |
| product    | text   | null: false |
| price      | integer| null: false |             |
| category   | string |             |
|user        | reference            |

user foreign_key

### Association

- belong_to:user
- has_one :orders

   

## orders テーブル

| Column   | Type       | Options                        |
| -------  | ---------- | ------------------------------ |
| item_id  | references |                                |
| user     | references |                                |

* item    foreign_key
* user    foreign_key
*

### Association

- belongs_to :item
- belongs_to :user
  belongs_to :address

## address テーブル
| Column   | Type       | Options                        |
| -------  | ---------- | ------------------------------ |
| postal   | integer    |                                |
| city     | text       |                                |
| address  | text       |                                |
| phone    | integer    |                                |


 
 belongs_to :oder
