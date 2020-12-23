# テーブル設計




## users テーブル


| Column   | Type   | Options     |
| -------- | ------ | ----------- |
|nick_name| string | null: false |
|first_name| string | null: false |
|last_name | string | null: false |
|fname_kana| string | null: false |
|lname_kana| string | null :false |
｜birthday  | date  | null :false |
| email    | string | unique: true|    validates :email, uniqueness: true
| encrypted_password | string | null: false   |



### Association
- has_many :items
- has_many :orders
- 
  

## items テーブル

| Column        | Type   | Options     |
| ------        | ------ | ----------- |
| item_name     | text   | null: false |
| price         | integer| null: false |             
| status_id     | integer| null: false |
| charge_id     | integer| null: false |
| region_id     | integer| null: false |
| date_id       | integer| null: false |
| category_id   | integer| null: false |
| user_id       | integer |user foreign_key|
             

* user foreign_key

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
* address foreign_key

### Association

- belongs_to :items
- belongs_to :users
  has_one    :addresses

## addresses テーブル
| Column   | Type       | Options       |
| -------  | ---------- | ------------- |
| postal   | string     |   null: false | 
| region_id| integer    |   null: false |                             
| city     | string       |   null: false |  
| build    | string       |   null: false |                         
| number   | string       |   null: false |                            
| phone    | string    |   null: false |                             


 
 belongs_to :oder
