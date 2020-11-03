# ProtospaceのER図

 ## usersテーブル

|  Column     |  Type     |  Option      |
| ------------|-----------|--------------|
|  email      |  string   |  null: false |
|  password   |  string   |  null: false |
|  name       |  string   |  null: false |
|  profile    |  text     |  null: false |
|  occupation |  text     |  null: false |
|  position   |  text     |  null: false |

### Association

- has_many :prototypes
- has_many :comments

## prototypesテーブル

| column     |  type       |  option      |
|------------|-------------|--------------|
|  title     |  string     |  null: false |
|  catch_copy|  text       |  null:false  |
|  image     |ActiveStorageで実装　　　　　　|
|  user      |  reference  |              |

### Association

- belongs_to :user
- has_many : comments

## commentsテーブル

| column     |  type       |  option      |
|------------|-------------|--------------|
|  text      |  text       |  null: false |
|  user      |  reference  |              |
|  prototyoe |  reference  |              |

- belongs_to :user
- belongs_to :prototype


