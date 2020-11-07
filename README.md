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
| birthday              | string     | null: false                    |

## items テーブル
| Column             | Type       | Options                        |
| ------------------ | ---------- | ------------------------------ |
| name               | string     | null: false                    |
| explanation        | string     | null: false                    |
| price              | integer    | null: false                    |
| category_id        | integer    | null: false                    |
| comments           | string     | null: false                    |
| user               | references | null: false, foreign_key: true |
| buy                | references | null: false, foreign_key: true |

## buys テーブル
| Column           | Type       | Options                        |
| ---------------- | ---------- | ------------------------------ |
| postcode         | string     | null: false                    |
| prefecture_id    | string     | null: false                    |
| city             | string     | null: false                    |
| block            | string     | null: false                    |
| building         | string     | null: false                    |
| phone_number     | string     | null: false                    |
| user             | references | null: false, foreign_key: true |
| item             | references | null: false, foreign_key: true |


