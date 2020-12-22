<<<<<<< Updated upstream
=======
<<<<<<< Updated upstream
=======
>>>>>>> Stashed changes
# テーブル設計

## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
<<<<<<< Updated upstream
| nick_name| string | null: false |
| name     | string | null: false |
| email    | string | null: false            |
| password | string | null: false            |
| profile  | text   | null: false            |
|occupation| text   | null: false            |
| position | text   | null: false            |

=======
|nick_name | string | null: false |
| name     | string | null: false |
| email    | string | null: false |
| password | string | null: false |
| birthday | date   | null: false  |
>>>>>>> Stashed changes



### Association
- has_many :item
<<<<<<< Updated upstream
- has_many :order
=======
- belong_to :order
>>>>>>> Stashed changes
- 
  

## items テーブル

| Column     | Type   | Options     |
| ------     | ------ | ----------- |
<<<<<<< Updated upstream
| product    | text   | null: false |
| price      | integer| null: false |             |
| category   | string |             |
|user        | reference            |

user foreign_key
=======
| product    | string | null: false |
| category   | text   | null: false |
| price      | integer| null: false |
| user       | reference            |

user    foreign_key

>>>>>>> Stashed changes

### Association

- belong_to:user
<<<<<<< Updated upstream
- has_one :orders
=======
- belong_to:order 
>>>>>>> Stashed changes

   

## orders テーブル

| Column   | Type       | Options                        |
| -------  | ---------- | ------------------------------ |
<<<<<<< Updated upstream
| item_id  | references |                                |
| user     | references |                                |
=======
| item_id | references |                                |
| user_id  | references |                                |
>>>>>>> Stashed changes

* item    foreign_key
* user    foreign_key
*

<<<<<<< Updated upstream
### Association

- belongs_to :item
- belongs_to :user
  belongs_to :address

## address テーブル

 belongs_to :oder
=======


- belongs_to :item
- belongs_to :user


## address テーブル

| Column     | Type   | Options     |
| ------     | ------ | ----------- |
| postal     | integer| null: false |
| category   | text   |             |
| city       | text   | null: false |
| order_id   | reference            |

### Association

belongs_to :order

order    foreign_key
>>>>>>> Stashed changes
>>>>>>> Stashed changes
