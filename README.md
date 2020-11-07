# README

# テーブル設計

## users テーブル
| Column                | Type       | Options                        |
| --------------------- | ---------- | ------------------------------ |
| username              | string     | null: false                    |
| email                 | string     | null: false                    |
| encrypted_password    | string     | null: false                    |
| first_name            | string     | null: false                    |
| last_name             | string     | null: false                    |
| first_name_ruby       | string     | null: false                    |
| last_name_ruby        | string     | null: false                    |
| birthday              | date       | null: false                    |

### Association

- has_many :items
- has_many :buys

## items テーブル
| Column             | Type       | Options                        |
| ------------------ | ---------- | ------------------------------ |
| name               | string     | null: false                    |
| explanation        | text       | null: false                    |
| price              | integer    | null: false                    |
| category_id        | integer    | null: false                    |
| status_id          | integer    | null: false                    |
| bearer_id          | integer    | null: false                    |
| shipping_area_id   | integer    | null: false                    |
| shipping_days_id   | integer    | null: false                    |
| user               | references | null: false, foreign_key: true |

### Association

- belongs_to :user
- has_one :buy_management

## buys テーブル
| Column           | Type       | Options                        |
| ---------------- | ---------- | ------------------------------ |
| postcode         | string     | null: false                    |
| prefecture_id    | integer    | null: false                    |
| city             | string     | null: false                    |
| block            | string     | null: false                    |
| building         | string     |                                |
| phone_number     | string     | null: false                    |
| buy_management   | references | null: false, foreign_key: true |

### Association

- belongs_to :user
- has_one :buy_management

## buy_management テーブル

| Column           | Type       | Options                        |
| ---------------- | ---------- | ------------------------------ |
| user             | references | null: false, foreign_key: true |
| item             | references | null: false, foreign_key: true |

### Association

- belongs_to :items
- belongs_to :buys


