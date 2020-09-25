# Vending Machine

#### 使用方法(すべてirbで実施)

ディレクトリに移動後、ファイルを読み込む

``require './vending_machine.rb'``

自動販売機をインスタンス化

``require './vending_machine.rb'``


##### 消費者の行動を想定した処理

通貨の投入処理をおこなう
```
#引数は10, 50, 100, 500, 1000のいずれか
vm.receive_money(500)
```
現在0購入可能な商品を表示する

`vm.available_products`

特定の商品が購入可能かを商品名で確認する

`vm.available?("コーラ")`

商品の購入処理をおこなう
```
# 引数には商品名を指定する
vm.dispense("コーラ")
```

お釣りを返却する

`vm.return_change`

管理者側の処理

売り上げ金額の確認

`vm.sales`

売り上げ金額をリセット

`vm.reset_sales`

ストックに新しい商品を追加する
```
#引数には「商品名、価格、追加する数」を順に指定
vm.stock.add_new_product("レッドブル", 200, 5)
```

ストックにすでに存在する商品の在庫数を増やす
```
#引数には「商品名、増やす数」を順に指定
vm.stock.restock("コーラ", 5)
```

ストックにすでに存在する商品の在庫数を減らす
```
#引数には「商品名、増やす数」を順に指定
vm.stock.remove("コーラ", 5)
```