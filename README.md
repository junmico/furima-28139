# README

# テーブル設計

## users テーブル

| Column      | Type       | Options     |
| ----------- | ---------- | ----------- |
| username    | string     | null: false |
| email       | string     | null: false |
| password    | string     | null: false |
| first_name  | string     | null: false |
| last_name   | string     | null: false |
| birthday    | string     | null: false |
| user_id     | references | null: false |

## items テーブル

| Column             | Type       | Options     |
| ------------------ | ---------- | ----------- |
| name               | string     | null: false |
| explanation        | string     | null: false |
| image              | string     | null: false |
| price              | string     | null: false |
| category           | string     | null: false |
| status             | string     | null: false |
| bearer             | string     | null: false |
| shipping_area      | string     | null: false |
| shipping_days      | string     | null: false |
| comments           | string     | null: false |
| user_id            | references | null: false |
| item_id            | references | null: false |

## buys テーブル

| Column    | Type       | Options                        |
| --------- | ---------- | ------------------------------ |
| adress    | string     | null: false, foreign_key: true |
| user_id   | references | null: false, foreign_key: true |
| item_id   | references | null: false, foreign_key: true |

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
