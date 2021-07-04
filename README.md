# README

## groups_usersテーブル

columns    |type   |option
-----------|-------|----------------
email      |string |null: false
password   |string |null: false
name       |string |null: false
profile    |text   |null: false
occupation |text   |null: false
position   |text   |null: false

### Association
-has_many :prototypes
-has_many :comments


## groups_prototypesテーブル

columns    |Type        |Option
-----------|------------|-------------------------------
title      |string      |null: false
catch_copy |text        |null: false
concept    |text        |null: false
user       |references  |null: false, foreign_key: true

### Association
-has_many :comments
-belongs_to :user


## groups_commentsテーブル

columns   |Type       |Option
----------|-----------|
text      |text       |null: false
user      |references |null: false, foreign_key: true
prototype |references |null: false, foreign_key: true

### Association
-belongs_to :user
-belongs_to :comment