# シフト管理システム
## 概要
本システムは,ウェブ上で雇用者と従業員の間でシフトの提出・承認ができるようにする
ことで,紙媒体でのシフトのやり取りと比べて,大幅な効率向上を図ることができる.
また、スプレッドシートでのスケジュール共有における編集の衝突問題,スケジュール管理ツール以外にもコミュニケーションが必要な問題点
を解決する目的がある. UIの利便性を考慮してカレンダーベースでのスケジュール登録を行うなどの取り組みも行っている.  
### 主要機能  
* アカウント機能
* シフト管理機能
* シフト承認機能(雇用者)
* ユーザ間のメッセージング機能
* 匿名の意見箱機能
* 周知事項のための掲示板機能
## 環境設定
Python 3.8.10 

Django 3.2

Django インストール
```
pip install Django==3.2
```
**UI用のモジュール**
```
pip install sympy
```
```
pip install django-widgets-improved
```
## ローカルでの動作
manage.pyのあるディレクトリで コマンドプロンプト
```
python manage.py runserver　
```
## DBの初期化
sqlite.dbは最初のサーバ上がり際に作られる
```
python manage.py createsuperuser
```
で最初のログイン用の管理者ユーザを作成する

## djangoの管理者サイトへのアクセス
http\://127.0.0.1:8000/admin で管理者ページにアクセスする
管理者サイト内で雇用者, 従業員のアカウント作成　所属店舗の登録等のDB操作を行う
