# BTCart ( BITCOIN & LIGHTNING SHOP CART END)





Start accepting Bitcoin payments on your website in minutes. Beautiful widgets, no fees, instant payouts over lightning or accept onchain payments. 

BUGS:
- RENAME PROPS
- Random Order ID Gen 
- ADD SHIPPING / Random Order ID + Instructions
- Only set one amount in Satoshi's 
- Change to shipping data / order
- Hide Bitcoin logo
- Show shipping info + Cart ( Live update on the right + Select Method)

There are 3 categories 
	1) Simple
	2) Widget
	3) Shopping Cart 

1) Simple

- Bitcoin QR + Scan to Pay Or link to mempool
- Lightning QR + Scan to Pay

2) Widget

- Fixed Amount 

- Free Donation Amount 

- Create Invoice Widget ( create your own custom invoice QR )
This will be the landing for Lightning.eu

3) Shopping Cart

- Standard Checkout Wizard

- Subscription Selection

# Variable Example

name="Kevin Gaethofs" 
accent="#000" 
to="sync@walletofsatoshi.com" 
addressbtc="bc1qk52y0erynfmfddnwvnrpn3dhm6gn60ce9duejw"
image="" 
shippingpay=0.0000025,
payamount=500000,
setpayamount=0.000005,
products="boots, boobs"
orderid="69"

## 🧑‍💻 Development

Checkout this repository and run the following commands to spin up a development server:

```
npm install
npm run serve
```

## Configuration options
 - `name`: The name being displayed on the widget
 - `image`: Path to the image that is displayed on the widget
 - `to`: Where the payments should be sent to ([Lightning Address](https://lightningaddress.com/))
 - `accent`: An accent color in RGB format to make your widget more colorful (i.e. `#20C997`)
 - `button-text`: The text to be displayed on the initial state of the widget (default: `Donate sats`)
 - `debug`: Debug mode, validates settings during initialization and displays configuration errors

**Example**
```
<lightning-widget 
    name="René Aaron" 
    accent="#20c997" 
    to="reneaaron@getalby.com" 
    image="https://secure.gravatar.com/avatar/07e22939e7672b38c56615068c4c715f?size=200" />
<script src="https://embed.twentyuno.net/js/app.js"></script>
```



