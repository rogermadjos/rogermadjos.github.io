**MD5 Private key**: `gdAFgbfgP4gDV25F`

**out\_trade_no**: `49f05be2585f4b35817c487140cd72d4`

**return_url**: `49f05be2585f4b35817c487140cd72d4`

**amount_str**: `100.00`

**partner_no**: `100070`

**buyer_name**: `Roger Madjos`

**buyer_contact**: `09958814009`

**good_name**: `MBS99 deposit`

**goods_detail**: `Deposit: 100`

**bank_code**: `ICBC`

**receiver_address**: `Earth`


## 1. Calculate digital signature

### a. The `plainText` is set as:
```http
partner_no=100070&service=gateway_pay&out_trade_no=49f05be2585f4b35817c487140cd72d4&amount_str=100.00&tran_ip=127.0.0.1&buyer_name=Roger%20Madjos&buyer_contact=09958814009&good_name=MBS99%20deposit&request_time=170209182236&return_url=http%3A%2F%2Ffcs.as2win.com%2Fnotify%2F49f05be2585f4b35817c487140cd72d4&verfication_code=gdAFgbfgP4gDV25F
```

### b. MD5 hash is calculated. The input encoding is `UTF-8` while the output encoding is `base64`: `8MQe3cPOr9m5B1uDVWzBdw==`

## 2. Form http request
```http
POST /gateway/pay HTTP/1.1
Host: service.lepayle.com
Content-Type: application/x-www-form-urlencoded
Cache-Control: no-cache

out_trade_no=49f05be2585f4b35817c487140cd72d4&return_url=http%3A%2F%2Ffcs.as2win.com%2Fnotify%2F49f05be2585f4b35817c487140cd72d4&amount_str=100.00&service=gateway_pay&partner_no=100070&input_charset=UTF-8&sign_type=MD5&request_time=170209182236&tran_ip=127.0.0.1&buyer_name=Roger+Madjos&buyer_contact=09958814009&good_name=MBS99+deposit&goods_detail=Deposit%3A+100&bank_code=ICBC&receiver_address=Earth&sign=8MQe3cPOr9m5B1uDVWzBdw%3D%3D
```
