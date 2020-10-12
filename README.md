## users テーブル
| Column    | Type   | Options    |
| --------- | ------ | ---------- |
| email     | string | null:false |
| password  | string | null:false |
| name      | string | null:false |
| profile   | text   | null:false |
| occupation| text   | null:false |
| position  | text   | null:false |
## アソシエーション
has_many :prototypes



## prototypes テーブル
| Column  | Type       | Options    |
| ------- | ---------- | ---------- |
| title   | string     | null:false |
| catch   | text       | null:false |
| concept | text       | null:false |
| user    | references |            |
## アソシエーション
belongs_to :user


## comments　テーブル
| Column    | Type       | Options    |
| --------- | ---------- | ---------- |
| text      | text       | null:false |
| user      | references |            |
| prototype | references |            |

