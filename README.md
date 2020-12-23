# テーブル設計



## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| nick_name| string | null: false |
|first_name| string | null: false |
|last_name | string | null: false |
|fname_kana| string | null: false |
|lname_kana| string | null :false |
| profile  | text   | null: false |
|occupation| text   | null: false |
| position | text   | null: false |
| email    | string | unique: true|    validates :email, uniqueness: true
| encrypted_password | string | null: false   |



### Association
- has_many :items
- has_many :orders
- 
  

## items テーブル

| Column     | Type   | Options     |
| ------     | ------ | ----------- |
| product    | text   | null: false |
| price      | integer| null: false |             
| Exhibitor  | text   | null: false |
| Status     | text   | null: false |
| charge     | text   | null: false |
| region     | text   | null: false |
| date       | date   | null: false |
| category   | string |             |
| image      | active storage       |
| user       | reference            |

user foreign_key

### Association

- belong_to:users
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

- belongs_to :items
- belongs_to :users
  belongs_to :addresses

## address テーブル
| Column   | Type       | Options                        |
| -------  | ---------- | ------------------------------ |
| postal   | integer    |                                |
| city     | text       |                                |
| address  | text       |                                |
| phone    | integer    |                                |


 
 belongs_to :oders
