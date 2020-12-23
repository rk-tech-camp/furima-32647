# テーブル設計



## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| nick_name| string | null: false |
|first_name| string | null: false |
|last_name | string | null: false |
|fname_kana| string | null: false |
|lname_kana| string | null :false |
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
| status     | text   | null: false |
| charge     | text   | null: false |
| region     | text   | null: false |
| date       | date   | null: false |
| category   | string |             |
| user_id    | integer              |

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
| Column   | Type       | Options       |
| -------  | ---------- | ------------- |
| postal   | integer    |   null: false |                             
| city     | text       |   null: false |                            
| address  | text       |   null: false |                            
| phone    | integer    |   null: false |                             


 
 belongs_to :oders
