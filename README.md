# Truewallet Voucher
เติมเงิน Truewallet ด้วยซองอั่งเปา

## Installation
```sh
npm i tw-vouncher-redeemer
```

## Examples
ตัวอย่างการเติมด้วยเลขข้างหลังซอง
```js
const tw = require('tw-vouncher-redeemer');

tw('เบอร์โทรศัพท์', 'xxxxxxxxxxxx').then(redeemed => {
    console.log(`redeem ซอง ${redeemed.code} ของ ${redeemed.owner_full_name} จำนวน ${redeemed.amount} บาทแล้ว`) 
}).catch(err => {
    console.error('invaild voucher code')
})
```
ตัวอย่างการเติมด้วยลิ้งค์ซอง
```js
const tw = require('tw-vouncher-redeemer');

tw('เบอร์โทรศัพท์', 'https://gift.truemoney.com/campaign/?v=xxxxfhFog10Ijbmg1c').then(redeemed => {
    console.log(`redeem ซอง ${redeemed.code} ของ ${redeemed.owner_full_name} จำนวน ${redeemed.amount} บาทแล้ว`) 
}).catch(err => {
    console.error('invaild voucher code')
})
```
