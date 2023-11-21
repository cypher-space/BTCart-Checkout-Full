# ⚡ Btc Pay

Start accepting Bitcoin payments on your website in minutes. Beautiful widgets, no fees, instant payouts.
Configuration modes include:

Bitcart ( Passes Order ID & Order Details & Amount )
Bitsub ( Subscription Options, ID, & Amount) 
Bitdonate ( Standard Widget), 
BitFix ( Current Widget )

- Bitcoin QR code 

## 🧑‍💻 Development

Checkout this repository and run the following commands to spin up a development server:

```
npm install
npm run serve
```

## Configuration options
 - `name`: The name being displayed on the widget
 - `image`: Path to the image that is displayed on the widget
 - `to`: Where the payments should be sent to 
 ([Lightning Address](https://lightningaddress.com/) or [LNURL](https://github.com/fiatjaf/lnurl-rfc))
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



