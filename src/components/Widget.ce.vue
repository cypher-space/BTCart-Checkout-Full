<template>
  <div v-cloak id="root" :style="cssProps">
    <canvas id="confetti" ref="confetti"></canvas>
    <div class="back">
      <a href="javascript:void(0)" @click="back()" v-if="step != 'start' && step != 'error' && step != 'thankyou'">
        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <g clip-path="url(#clip0_27_452)">
            <path class="inherit-textcolor"
              d="M13.8994 6.99833e-10L4.70703 9.19239C4.3165 9.58291 4.3165 10.2161 4.70703 10.6066L13.8994 19.799"
              stroke="white" stroke-width="2" stroke-linecap="round" />
          </g>
          <defs>
            <clipPath id="clip0_27_452">
              <rect width="20" height="20" fill="white" />
            </clipPath>
          </defs>
        </svg>

      </a>
    </div>
    <div class="card" v-bind:style="backgroundImageStyle">
      <Transition name="fade" mode="out-in">
        <div v-if="step == 'start'">
          <!-- <div><img v-if="image" class="image" :src="image" width="150" height="150" :alt="name" /></div>
           -->

           <svg xmlns="http://www.w3.org/2000/svg" xml:space="preserve" width="100%" height="100%" version="1.1" shape-rendering="geometricPrecision" text-rendering="geometricPrecision" image-rendering="optimizeQuality" fill-rule="evenodd" clip-rule="evenodd"
viewBox="0 0 4257.46 889.51"
 xmlns:xlink="http://www.w3.org/1999/xlink"
 xmlns:xodm="http://www.corel.com/coreldraw/odm/2003">
 <g id="Layer_x0020_1">
  <metadata id="CorelCorpID_0Corel-Layer"/>
  <g id="_1421487920208">
   <path fill="#F7931A" fill-rule="nonzero" d="M875.92 551.95c-59.08,238.24 -300.11,383.47 -538.36,324.39 -238.24,-59.07 -383.47,-300.11 -324.39,-538.35 59.08,-238.25 300.11,-383.49 538.35,-324.41 0.4,0.1 0.81,0.2 1.21,0.31 237.61,59.63 382.17,300.28 323.19,538.06z"/>
   <path fill="white" fill-rule="nonzero" d="M545.37 380.28c-13.89,55.56 -98.61,27.08 -126.11,20.28l24.3 -97.22c27.08,6.67 115.7,19.44 101.39,76.94l0.42 0zm-15.14 157.1c-15,60.54 -116.94,27.78 -150,19.57l26.8 -107.36c33.06,8.33 138.89,24.58 123.2,87.79zm111.11 -156.26c8.75,-59.17 -36.25,-90.97 -97.22,-112.08l20 -80.14 -49.3 -12.22 -19.44 78.06c-12.78,-3.19 -25.97,-6.25 -39.03,-9.17l19.44 -78.89 -48.75 -12.22 -20 80.14 -31.11 -6.94 -67.36 -16.81 -12.92 52.09c0,0 36.11,8.33 35.42,8.89 13.79,1.67 23.85,13.92 22.78,27.78l-22.78 91.25c1.71,0.39 3.39,0.94 5,1.67l-5.14 -1.39 -31.81 127.92c-2.98,9.36 -12.98,14.51 -22.35,11.53l-0.01 0c0,0.69 -35.56,-8.75 -35.56,-8.75l-24.17 55.56 63.47 15.7 34.72 9.03 -20.14 80.97 48.75 12.22 20 -80.14c13.14,3.61 26.07,6.94 38.75,10l-19.72 80.42 48.75 12.08 20.14 -80.83c83.33,15.71 145.69,9.44 172.08,-65.83 21.25,-60.56 -1.11,-95.42 -44.86,-118.2 31.94,-7.36 55.56,-27.78 62.36,-71.67z"/>
   <path fill="#4D4D4D" fill-rule="nonzero" d="M1157.17 750c25.96,0.08 51.5,-6.53 74.17,-19.17 23.33,-12.44 43.85,-29.57 60.28,-50.28 17.12,-21.9 30.58,-46.43 39.86,-72.64 9.79,-27.08 14.76,-55.65 14.72,-84.44 1.56,-29.21 -4.68,-58.31 -18.06,-84.31 -11.94,-20.14 -34.17,-30.41 -66.39,-30.41 -14.04,0.48 -28,2.39 -41.67,5.69 -16.97,3.79 -32.67,11.93 -45.56,23.61l-73.61 307.78 11.81 2.22c3.51,0.86 7.1,1.42 10.69,1.67 4.61,0.57 9.25,0.8 13.89,0.69l19.86 -0.42zm146.25 -481.11c32.15,-0.74 64.07,5.82 93.33,19.17 25.4,12.11 47.72,29.82 65.28,51.81 17.98,22.74 31.2,48.85 38.89,76.8 8.42,30.82 12.57,62.64 12.36,94.59 -0.04,99.4 -38.57,194.91 -107.5,266.53 -33.42,34.28 -73.18,61.72 -117.08,80.83 -46.03,20.26 -95.82,30.59 -146.11,30.28l-35.56 0c-19.33,-0.63 -38.63,-2.29 -57.78,-5 -23.39,-3.39 -46.57,-8.02 -69.44,-13.89 -23.98,-5.69 -47.26,-13.98 -69.44,-24.72l195.14 -817.5 174.31 -27.78 -69.44 290.14c14.46,-6.54 29.47,-11.79 44.86,-15.69 15.86,-3.86 32.15,-5.78 48.47,-5.69l-0.28 0.14z"/>
   <path fill="#4D4D4D" fill-rule="nonzero" d="M1774.39 209.3c-22.72,0.22 -44.87,-7.06 -63.06,-20.69 -19.28,-15.25 -29.7,-39.1 -27.78,-63.61 -0.08,-15.29 3.18,-30.42 9.58,-44.31 6.13,-13.53 14.74,-25.78 25.42,-36.11 10.67,-10.14 23.03,-18.32 36.53,-24.17 14.04,-6.03 29.17,-9.1 44.44,-9.03 22.56,-0.07 44.5,7.25 62.5,20.83 19.24,15.28 29.65,39.11 27.78,63.61 0.12,15.33 -3.1,30.5 -9.44,44.44 -6.13,13.46 -14.7,25.65 -25.28,35.97 -10.64,10.18 -23,18.36 -36.53,24.17 -14.04,6.03 -29.17,9.06 -44.44,8.89l0.28 0zm-80.97 663.76l-166.67 0 140.83 -591.68 167.64 0 -141.81 591.68z"/>
   <path fill="#4D4D4D" fill-rule="nonzero" d="M1981.06 134.03l174.3 -26.94 -43.33 174.31 186.68 0 -33.63 137.22 -185.14 0 -49.44 206.39c-4.28,15.8 -6.93,32 -7.92,48.35 -1.02,13.22 0.94,26.5 5.69,38.87 4.65,11.1 13.26,20.07 24.17,25.14 15.7,6.94 32.84,10.1 50,9.17 17.58,0.06 35.12,-1.67 52.36,-5.14 17.35,-3.39 34.44,-8.03 51.11,-13.89l12.5 128.33c-23.93,8.6 -48.38,15.71 -73.2,21.25 -30.67,6.51 -61.98,9.54 -93.33,9.03 -51.81,0 -91.81,-7.78 -120.42,-23.06 -26.76,-13.61 -48.2,-35.81 -60.83,-63.06 -12.33,-28.91 -17.71,-60.31 -15.69,-91.67 1.87,-36.79 7.12,-73.33 15.69,-109.17l110.42 -465.69 0 0.56z"/>
   <path fill="#4D4D4D" fill-rule="nonzero" d="M2292.59 636.8c-0.35,-49.08 8.01,-97.86 24.72,-144.02 15.67,-43.65 39.74,-83.8 70.83,-118.19 31.35,-34.11 69.47,-61.26 111.94,-79.74 46.32,-20 96.35,-29.99 146.8,-29.29 30.46,-0.36 60.86,2.85 90.56,9.57 24.97,5.92 49.26,14.39 72.5,25.28l-57.91 130.14c-15,-6.11 -30.56,-11.37 -46.67,-16.25 -19.21,-5.35 -39.1,-7.83 -59.03,-7.36 -50.36,-1.82 -98.8,19.47 -131.53,57.78 -32.5,38.23 -48.81,89.62 -48.89,154.17 -1.53,32.74 7.11,65.14 24.72,92.79 16.47,23.61 46.86,35.4 91.11,35.4 21.21,0.02 42.35,-2.26 63.06,-6.8 18.47,-3.94 36.57,-9.56 54.03,-16.81l12.36 133.9c-22.72,8.6 -45.9,15.93 -69.44,21.93 -29.89,6.74 -60.47,9.92 -91.11,9.46 -40.67,1.18 -81.15,-5.67 -119.17,-20.15 -30.22,-12.18 -57.43,-30.8 -79.72,-54.57 -21.15,-23.04 -36.78,-50.6 -45.69,-80.57 -9.43,-31.54 -14.11,-64.31 -13.89,-97.22l0.42 0.56z"/>
   <path fill="#4D4D4D" fill-rule="nonzero" d="M3114.94 407.5c-23.5,-0.33 -46.47,7.14 -65.28,21.25 -19.07,14.76 -35.07,33.13 -47.08,54.03 -13.21,22.25 -23.13,46.31 -29.44,71.41 -6.11,24.06 -9.29,48.76 -9.44,73.59 -1.5,30.31 4.67,60.49 17.92,87.78 12.09,20.97 33.75,31.53 65.28,31.53 23.54,0.4 46.54,-7.13 65.28,-21.39 19.11,-14.76 35.14,-33.13 47.22,-54.01 13.02,-22.28 22.7,-46.33 28.76,-71.41 6.04,-24.11 9.22,-48.87 9.43,-73.75 1.56,-30.29 -4.63,-60.5 -17.92,-87.78 -12.08,-20.83 -33.89,-31.39 -65.28,-31.39l0.56 0.14zm-83.33 481.39c-35.39,0.82 -70.58,-5.32 -103.61,-18.06 -27.79,-10.96 -52.61,-28.26 -72.5,-50.56 -19.56,-22.46 -34.29,-48.69 -43.33,-77.08 -9.82,-31.83 -14.52,-65.03 -13.89,-98.33 0.11,-45.86 7.46,-91.43 21.82,-135 13.93,-43.85 35.68,-84.82 64.15,-120.97 28.6,-36.14 64.17,-66.18 104.58,-88.33 43.5,-23.39 92.28,-35.21 141.67,-34.31 35.18,-0.64 70.18,5.5 103.06,18.06 27.82,10.78 52.78,27.85 72.91,49.86 19.44,22.52 34.14,48.74 43.2,77.08 9.89,31.86 14.58,65.11 13.89,98.47 -0.14,45.82 -7.31,91.36 -21.25,135 -13.69,43.91 -35.04,85.04 -63.06,121.53 -28.18,36.29 -63.61,66.33 -104.03,88.2 -44.17,23.51 -93.58,35.37 -143.61,34.44z"/>
   <path fill="#4D4D4D" fill-rule="nonzero" d="M3626.75 209.3c-22.68,0.24 -44.81,-7.04 -62.91,-20.69 -19.29,-15.25 -29.71,-39.1 -27.78,-63.61 -0.08,-15.29 3.18,-30.42 9.57,-44.31 5.96,-13.46 14.33,-25.69 24.72,-36.11 10.74,-10.11 23.14,-18.29 36.67,-24.17 14,-6.02 29.08,-9.09 44.32,-9.03 22.72,-0.2 44.91,7.14 63.06,20.83 19.24,15.28 29.64,39.11 27.78,63.61 0.03,15.35 -3.29,30.52 -9.74,44.44 -6.02,13.47 -14.56,25.68 -25.13,35.97 -10.64,10.18 -23,18.36 -36.53,24.17 -13.92,5.97 -28.9,9 -44.04,8.89zm-80.82 663.76l-166.67 0 140.56 -591.68 167.78 0 -141.67 591.68z"/>
   <path fill="#4D4D4D" fill-rule="nonzero" d="M3807.59 308.33c12.64,-3.61 26.67,-8.06 41.67,-12.91 15,-4.86 32.5,-9.31 51.79,-13.89 21.17,-4.49 42.54,-7.87 64.04,-10.14 26.71,-2.82 53.56,-4.17 80.42,-4.03 87.78,0 148.33,25.5 181.67,76.53 19.96,30.56 30.06,67.84 30.3,111.85l0 3.17c-0.15,28.62 -4.42,60.05 -12.8,94.28l-76.53 319.44 -167.22 0 74.3 -312.79c4.44,-19.43 8.06,-38.32 10.7,-56.79 2.89,-15.99 2.89,-32.36 0,-48.33 -2.76,-13.35 -10.14,-25.29 -20.83,-33.75 -14.82,-9.72 -32.46,-14.26 -50.14,-12.92 -22.26,0.04 -44.46,2.32 -66.25,6.81l-109.17 458.33 -168.21 0 136.26 -564.86z"/>
  </g>
 </g>
</svg>


            <div>
            <h3>Choose your payment method</h3>
          </div>
          <div>
            <button type="button" class="button margins" @click="showAmount()">⚡️ Lightning Network </button>

            <button type="button" class="button margins" @click="showAmount()">⛓️ Onchain Transaction </button>


          </div>
        </div>
        <div v-else-if="step == 'amount'">
          <div>
            <h3>Total Bitcoin to pay</h3>
            <h1>{{ this.setAmount }}</h1>
            <h3>{{ this.convertFiat }} dollar</h3>
            <h4>Curent bitcoin price {{ this.btcprice }} $</h4>
            <h5>provided by YieldMonitor.io</h5>
            <!-- <h4>Change Fiat Estimate</h4> -->

          </div>
          <div class="mb-1">
            <div class="pill-container">

              <!-- <div class="pill" >EURO </div>


              <div class="pill" >DOLLAR</div> -->

              <!-- <div class="pill" v-bind:key="item.amount" v-for="item in amountList" @click="currentAmount = item.amount">{{
                item.label }}</div> -->
            </div>
            <!-- <input type="number" class="mb-1" name="amount" placeholder="Enter an amount" required
              v-model.number="currentAmount" /> -->
              
          </div>
          <div>
            <button type="button" class="button" @click="showNote()">Next</button>
          </div>
        </div>
        <div v-else-if="step == 'note'">
          <h3>Order ID: {{ this.orderid }}</h3>
          <input v-model="comment" class="hidden" />
          <p>
          Products: <br><span> {{ this.products }}</span>
        </p>
        <!-- <p>
          Quantity:<br><span> {{ this.order.amount }}</span>
        </p> -->
        <p>
          Shipping:<br><span> {{ this.shippingpay }}</span>
        </p>
          
          
          
          
          
          
          
          <button type="button" class="button" @click="step = 'pay'; pay()">Proceed To Pay</button>
        </div>
        <div v-else-if="step == 'pay'">
          <svg width="100" height="100" viewBox="0 0 38 38" xmlns="http://www.w3.org/2000/svg">
            <defs>
              <linearGradient x1="8.042%" y1="0%" x2="65.682%" y2="23.865%" id="a">
                <stop :stop-color="color" stop-opacity="0" offset="0%" />
                <stop :stop-color="color" stop-opacity=".631" offset="63.146%" />
                <stop :stop-color="color" offset="100%" />
              </linearGradient>
            </defs>
            <g fill="none" fill-rule="evenodd">
              <g transform="translate(1 1)">
                <path d="M36 18c0-9.94-8.06-18-18-18" id="Oval-2" stroke="url(#a)" stroke-width="2">
                  <animateTransform attributeName="transform" type="rotate" from="0 18 18" to="360 18 18" dur="0.9s"
                    repeatCount="indefinite" />
                </path>
                <circle fill="#fff" cx="36" cy="18" r="1">
                  <animateTransform attributeName="transform" type="rotate" from="0 18 18" to="360 18 18" dur="0.9s"
                    repeatCount="indefinite" />
                </circle>
              </g>
            </g>
          </svg>
          <h4 class="mb-2">Waiting for payment with your browser wallet...</h4>
          <a href="javascript:void(0)" @click="showQR()" v-if="paymentType == 'Invoice'">
            <svg style="vertical-align: middle" width="20" height="20" viewBox="0 0 20 20" fill="none"
              xmlns="http://www.w3.org/2000/svg">
              <rect class="map-stroke-color" x="3.75" y="3.75" width="3" height="3" stroke="white" stroke-width="1.5" />
              <rect class="map-stroke-color" t x="13.2499" y="3.75" width="3" height="3" stroke="white"
                stroke-width="1.5" />
              <rect class="map-stroke-color" x="3.75" y="13.25" width="3" height="3" stroke="white" stroke-width="1.5" />
              <rect class="map-fill-color" x="3" y="9.25" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="6" y="9.25" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="9.16663" y="9.25" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="9.16663" y="12.375" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="9.16663" y="15.5" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="9.16663" y="6.125" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="9.16663" y="3" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="12.3333" y="9.25" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="15.4999" y="9.25" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="12.3333" y="12.375" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="15.4999" y="12.375" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="12.3333" y="15.5" width="1.5" height="1.5" fill="white" />
              <rect class="map-fill-color" x="15.4999" y="15.5" width="1.5" height="1.5" fill="white" />
            </svg>
            Use QR code
          </a>
        </div>
        <div v-else-if="step == 'qr'">
          <div class="mb-1">
            <a :href="'lightning:' + paymentRequest">
              <!-- <img class="qr" width="150" height="150" :src="'https://embed.twentyuno.net/qr/' + paymentRequest"
                alt="qr" /> -->
                <img :src="qrCodeDataUrl" class="qr" width="150" height="150" alt="QR Code" />
            </a>
          </div>
          <Transition name="fade" mode="out-in">
            <h4 class="qr-heading" v-if="!qrTimeoutElapsed">Scan or Click to pay</h4>
            <button v-else class="button" @click="step = 'thankyou'; celebrate()">Done?</button>
          </Transition>
        </div>
        <div v-else-if="step == 'thankyou'">
          <!-- <div><img v-if="image" class="image" :src="image" width="150" height="150" :alt="name" /></div> -->
          <div>
            <h3>Thank you, Your order is recieved!</h3>
          </div>
          <!-- <div>
            <button class="button" @click="reset(); step = 'start'">Start over</button>
          </div> -->
        </div>
        <div v-else-if="step == 'error'">
          <h3 style="margin-bottom: 0">{{ errorTitle }}</h3>
          <p class="mb-2" v-html="errorMessage">
          </p>
          <button class="button" @click="reset(); step = 'start'">Start over</button>
        </div>
      </Transition>
    </div>
  </div>
</template>
<script>
import JSConfetti from 'js-confetti'
import { fetchInvoice, fetchParams, contrastingColor, luma, formatAmount } from './utils/helpers';
import QRCode from 'qrcode';


export default {
  name: "LightningWidget",
  props: {
    name: { type: String, required: true },
    to: { type: String, required: true, default: "sync@walletofsatoshi.com" },

    amounts: { type: String, required: false, default: "Euro,Dollar" },
    labels: { type: String, required: false },

    // Order
    products: { type: String, default:'stickers, books, tshirt' },
    orderid: { type: String, default:'13' },

    // Style
    image: { type: String, required: true },
    accent: { type: String, default: '#20C997' },
    buttonText: { type: String, default: 'Donate sats' },
    backgroundImage: { type: String, default: null },

    // Deprecated --> use `to`
    address: { type: String, required: false, default: "reneaaron@getalby.com" },

    // Debugging purposes only 
    debug: { type: Boolean, default: false },
    initialStep: { type: String, default: 'start' },

    // Amounts
    payamount: {type: Number, default: 800},
    setpayamount: {type: Number, default: 0.00008},
    shippingpay: {type: Number, default: 0.00003},

  },
  data() {
    return {
      currentAmount: this.payamount,
      setAmount: this.setpayamount,
      convertFiat: '',
      params: {},
      loading: false,
      paymentRequest: null,
      step: this.initialStep,
      comment: this.orderid,
      qrTimeoutElapsed: false,
      paymentType: 'Invoice',
      errorTitle: '',
      btcprice:'',
      errorMessage: '',
      qrCodeDataUrl: '',
      amountList: [],
    };
  },
  computed: {
    cssProps() {
      return {
        '--accent': this.accent,
        '--color': this.color,
        '--button-color': luma(this.accent.substring(1)) < 200 ? this.accent : '#000',
      }
    },
    color() {
      return contrastingColor(this.accent.substring(1));
    },
    backgroundImageStyle() {
      return this.backgroundImage ? { 'background-image': `url('${this.backgroundImage}')` } : {};
    }
    
  },
  async mounted() {




    const labels = this.labels ? this.labels.split(",") : [];
    this.amountList = this.amounts.split(",").slice(0, 3).map((x, i) => {
      return {
        label: labels[i] ?? formatAmount(parseInt(x), 0),
        amount: parseInt(x)
      };
    });

    // Install fonts (do need to be included outside of the shadow dom)
    const fontImport = document.createElement("link");
    fontImport.setAttribute("href", "https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap");
    fontImport.setAttribute("rel", "stylesheet");
    fontImport.setAttribute("type", "text/css");

    document.head.appendChild(fontImport);

    this.fetchBitcoinPrice();
    // Keysend payments
    if (this.to.match(/^[0-9a-fA-F]{66}$/i)) {
      this.paymentType = "Keysend";
    }
    else if (this.debug) {
      try {
        this.params = await fetchParams(this.to);
        const minAmount = this.amountList.reduce((a, b) => Math.max(a.amount, b.amount));
        const maxAmount = this.amountList.reduce((a, b) => Math.min(a.amount, b.amount));
        if (this.params.min > minAmount || this.params.max < maxAmount) {
          this.error("Configuration error", `Please make sure the LNURL you provided allows payments between ${minAmount} and ${maxAmount} sats. (min: ${this.params.min}, max: ${this.params.max})`);
        }
      }
      catch (e) {
        this.error("Configuration error", "Are you sure this is a valid lightning address or LNURL?");
      }
    }
  },
  methods: {
    error: function (title, message) {
      this.errorTitle = title;
      this.errorMessage = message;
      this.step = 'error';
    },
    pay: async function () {
      await this['pay' + this.paymentType]();

          QRCode.toDataURL(this.paymentRequest, (error, dataUrl) => {
            if (error) {
              console.error('Error generating QR code:', error);
            } else {
              this.qrCodeDataUrl = dataUrl;
            }
          });


    },

    fetchBitcoinPrice() {
      fetch('https://app.yieldmonitor.io/api/v2/symbol/ym/33913')
        .then(response => {
          if (!response.ok) {
            throw new Error('Network response was not ok');
          }
          return response.json();
          
        })
        .then(data => {
          this.btcprice = Number(data.symbols[0].price).toFixed(2)
          this.convertFiat = (Number(this.btcprice) * Number(this.setAmount)).toFixed(2)
          // this.btcprice = Number(data._rawValue
          // console.log(datasub)
        })
        .catch(error => {
          console.error('Error fetching Bitcoin price:', error);
          // Handle error (e.g., set btcprice to a default value or show an error message)
        });
    },

    payKeysend: async function () {
      let error = false;

      try {
        this.loading = true;

        if (window.webln) {
          await window.webln.enable();
          await window.webln.keysend({
            destination: this.to,
            amount: this.currentAmount,
            customRecords: {
              // https://docs.lightning.engineering/lightning-network-tools/lnd/send-messages-with-keysend
              34349334: this.comment
            }
          });

          this.step = 'thankyou';
          this.celebrate();

        } else {
          error = true;
        }
      } catch (e) {
        error = true;
      } finally {
        this.loading = false;
      }

      if (error) {
        this.error("No wallet available", `You first need to install a browser extension.<br><br><a class="text-link" href="https://www.getalby.com" target="_blank" rel="noopener noreferrer">Learn more</a>`);
      }
    },
    payInvoice: async function () {
      let webln;
      let error = false;

      try {
        this.loading = true;
        let invoice;

        // Fetch invoice
        try {
          invoice = await fetchInvoice(this.to || this.address, this.currentAmount, this.comment);
          this.paymentRequest = invoice.payment_request;
        }
        catch (e) {
          this.error('Sorry', 'An error happend during the payment. Try again?');
          this.loading = false;
          return;
        }

        webln = window.webln;
        if (webln) {
          await webln.enable();
          await webln.sendPayment(invoice.payment_request);

          this.step = 'thankyou';
          this.celebrate();

        } else {
          error = true;
        }
      } catch (e) {
        error = true;
      } finally {
        this.loading = false;
      }

      if (error) {
        this.showQR();
      }
    },
    showAmount: async function() {
      this.params = await fetchParams(this.to);
      this.step = 'amount';
    },
    showNote: function() {
      if(this.currentAmount <= 0)
        return;

      if(this.params.commentAllowed > 0) {
        this.step = 'note';
      } else {
        this.step = 'pay';
        this.pay();
      }
    },
    showQR: function () {
      this.qrTimeoutElapsed = false;
      this.step = 'qr';
      setTimeout(() => { this.qrTimeoutElapsed = true; }, 3000);
    },
    back: function () {
      const steps = [
        'start',
        'amount',
        'note',
        'pay',
        'qr',
      ];

      this.step = steps[steps.indexOf(this.step) - 1];
    },
    celebrate: function () {
      const canvas = this.$refs["confetti"];
      const jsConfetti = new JSConfetti({ canvas });
      jsConfetti.addConfetti({
        confettiColors: [
          this.color
        ],
      });
    },
    reset: function () {
      this.comment = '';
      this.currentAmount = null;
      this.paymentRequest = null;
    }
  },
};
</script>

<style>
/* Reset CSS */
abbr,
address,
article,
aside,
audio,
b,
blockquote,
body,
canvas,
caption,
cite,
code,
dd,
del,
details,
dfn,
div,
dl,
dt,
em,
fieldset,
figcaption,
figure,
footer,
form,
h1,
h2,
h3,
h4,
h5,
h6,
header,
hgroup,
html,
i,
iframe,
img,
ins,
kbd,
label,
legend,
li,
mark,
menu,
nav,
object,
ol,
p,
pre,
q,
samp,
section,
small,
span,
strong,
sub,
summary,
sup,
table,
tbody,
td,
tfoot,
th,
thead,
time,
tr,
ul,
var,
video {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent
}

body {
  line-height: 1
}

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
  display: block
}

nav ul {
  list-style: none
}

blockquote,
q {
  quotes: none
}

.hidden{
  display: none;
}

blockquote:after,
blockquote:before,
q:after,
q:before {
  content: "";
  content: none
}

a {
  margin: 0;
  padding: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent
}

ins {
  text-decoration: none
}

ins,
mark {
  background-color: #ff9;
  color: #000
}

mark {
  font-style: italic;
  font-weight: 700
}

del {
  text-decoration: line-through
}

abbr[title],
dfn[title] {
  border-bottom: 1px dotted;
  cursor: help
}

table {
  border-collapse: collapse;
  border-spacing: 0
}

hr {
  display: block;
  height: 1px;
  border: 0;
  border-top: 1px solid #ccc;
  margin: 1em 0;
  padding: 0
}

input,
select {
  vertical-align: middle
}

@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');

* {
  font-family: "Inter", sans-serif;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease-in-out;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

#root {
  position: relative;
  min-width: 250px;
  width: 100%;
}

.card {
  box-shadow: 0px 32px 32px rgba(0, 0, 0, 0.07), 0px 16px 16px rgba(0, 0, 0, 0.07), 0px 8px 8px rgba(0, 0, 0, 0.07), 0px 4px 4px rgba(0, 0, 0, 0.07), 0px 2px 2px rgba(0, 0, 0, 0.07);
  border-radius: 25px;
  color: var(--color);
  padding: 25px;
  background-color: var(--accent);
  min-height: 290px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-size: cover;
  background-position: center center;
}

.card>div {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.qr {
  background: #FFFFFF;
  box-shadow: 0px 32px 32px rgba(0, 0, 0, 0.07), 0px 16px 16px rgba(0, 0, 0, 0.07), 0px 8px 8px rgba(0, 0, 0, 0.07), 0px 4px 4px rgba(0, 0, 0, 0.07), 0px 2px 2px rgba(0, 0, 0, 0.07);
  border-radius: 5px;
  padding: 8px;
}

.mb-1 {
  margin-bottom: 1em;
}

.mb-2 {
  margin-bottom: 2em;
}

.button {
  font-size: 17px;
  background: #FFFFFF;
  box-shadow: 0px 32px 32px rgba(0, 0, 0, 0.07), 0px 16px 16px rgba(0, 0, 0, 0.07), 0px 8px 8px rgba(0, 0, 0, 0.07), 0px 4px 4px rgba(0, 0, 0, 0.07), 0px 2px 2px rgba(0, 0, 0, 0.07);
  border-radius: 50px;
  padding: 10px 30px;
  border: none;
  flex: none;
  color: var(--button-color);
  font-weight: bold;
  border: 1px solid transparent;
  transition: all 0.1s ease-in;
}

.margins{
  margin: 10px ;
}

.button:hover {
  cursor: pointer;
  background: var(--accent);
  border: 1px solid #FFF;
  color: var(--color);
}

.card .image {
  background: #FFFFFF;
  box-shadow: 0px 32px 32px rgba(0, 0, 0, 0.07), 0px 16px 16px rgba(0, 0, 0, 0.07), 0px 8px 8px rgba(0, 0, 0, 0.07), 0px 4px 4px rgba(0, 0, 0, 0.07), 0px 2px 2px rgba(0, 0, 0, 0.07);
  border-radius: 100px;
  max-width: 150px;
}

.logo {
  position: absolute;
  top: 16px;
  right: 16px;
}

textarea {
  max-width: 90%;
  background: none;
  border: none;
  outline: none;
  resize: none;
  text-align: center;
  color: var(--color);
  font-size: 17px;

}

textarea::placeholder {
  color: var(--color);
  opacity: 0.5;
}

input {
  font-size: 17px;
  border: none;
  border-radius: 50px;
  padding: 10px 20px;
  text-align: center;
  color: var(--button-color);
  font-weight: bold;
  outline: none;
  font-size: 16px;
  max-width: 200px;
}

input::placeholder {
  color: var(--button-color);
  opacity: 0.5;
}

input[type="number"] {
  -moz-appearance: textfield;
}

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
}

a,
a:visited,
a:active,
a:hover {
  color: var(--color);
  font-weight: 500;
  text-decoration: none;
}

.pill {
  font-size: 17px;
  border: 1px solid var(--color);
  color: var(--color);
  padding: 0.5em 1em;
  border-radius: 50px;
  flex-grow: 1;
  text-align: center;
  margin-bottom: 1em;
  margin-left: 0.25em;
  margin-right: 0.25em;
  cursor: pointer;
}

.pill:hover {
  color: var(--accent);
  background: var(--color);
}

.pill-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.back {
  position: absolute;
  top: 15px;
  left: 15px;
  z-index: 10;
}

#confetti {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 25px;
  pointer-events: none;
}

h1 {
  font-size: 44px;
  margin: 1em;
  line-height: 29px;

}

h3 {
  font-size: 24px;
  margin: 1em;
  line-height: 29px;
}

h4 {
  font-size: 17px;
  margin: 1em;
  line-height: 21px;
}

h5 {
  font-size: 10px;
  margin: 1em;
  line-height: 21px;
}

p {
  margin: 1em 0;
  line-height: 1.5em;
}

a.text-link,
a.text-link:hover,
a.text-link:visited,
a.text-link:active {
  color: var(--color);
  text-decoration: underline;
}

/* Conditional SVG fill / stroke colors */
.inherit-textcolor,
.map-stroke-color {
  stroke: var(--color);
}

.map-fill-color {
  fill: var(--color);
}

.qr-heading {
  text-align: center;
  margin: 0;
}</style>