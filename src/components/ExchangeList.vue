<template>
  <div class="exchange-list">
    <b-container>
      <b-row v-if="markets" class="justify-content-md-center">
        <b-col md="auto" v-for="market in markets" :key="market.pair">
          <b-card-group class="markets">
              <b-card
                :img-src="market.logo"
                img-alt="Image"
                img-top
                tag="article"
                class="mb-3"
              >
                <b-card-text>
                  <div>
                    <span>Price:</span> {{market.price}}
                  </div>
                  <div>
                    <span>Pair:</span> {{market.pair}}
                  </div>
                </b-card-text>

                <div class="text-center">
                  <b-button size="sm" :href="market.link" variant="dark" target="_blank">Visit Exchange</b-button>
                </div>
              </b-card>
          </b-card-group>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'ExchangeList',
  data() {
    return  {
      markets: [
        {
          market: "FORKDELTA",
          price: "",
          pair: "PPI-ETH",
          logo: "https://raw.githubusercontent.com/piedpipercoin-project/website/master/src/assets/markets/forkdelta.png",
          link: "https://forkdelta.app/#!/trade/0x5a3c9a1725aa82690ee0959c89abe96fd1b527ee-ETH"
        },
        {
          market: "DDEX",
          price: "",
          pair: "PPI-WETH",
          logo: "https://raw.githubusercontent.com/piedpipercoin-project/website/master/src/assets/markets/ddex.png",
          link: "https://ddex.io/trade/PPI-WETH"
        },
        {
          market: "IDAX",
          price: "",
          pair: "PPI-BTC",
          logo: "https://raw.githubusercontent.com/piedpipercoin-project/website/master/src/assets/markets/idax.png",
          link: "https://www.idax.pro/exchange?pairname=PPI_BTC"
        },
        {
          market: "SATURNNETWORK",
          price: "",
          pair: "PPI-ETH",
          logo: "https://raw.githubusercontent.com/piedpipercoin-project/website/master/src/assets/markets/saturnnetwork.png",
          link: "https://www.saturn.network/exchange/ETH/order-book/0x5a3c9a1725aa82690ee0959c89abe96fd1b527ee/0x0000000000000000000000000000000000000000"
        },
        {
          market: "BAMBOORELAY",
          price: "",
          pair: "PPI-WETH",
          logo: "https://raw.githubusercontent.com/piedpipercoin-project/website/master/src/assets/markets/bamboorelay.png",
          link: "https://bamboorelay.com/trade/PPI-WETH"
        },
        {
          market: "CRYPTOBRIDGE",
          price: "",
          pair: "PPI-BTC",
          logo: "https://raw.githubusercontent.com/piedpipercoin-project/website/master/src/assets/markets/cryptobridge.png",
          link: "https://wallet.crypto-bridge.org/market/BRIDGE.PPI_BRIDGE.BTC"
        }
      ],
      errors: []
    }
  },
  created() {
    axios.get('https://middle-out.herokuapp.com/exchanges')
    .then(response => {
      this.markets = response.data.data.exchanges
    })
    .catch(e => {
      this.errors.push(e)
    })
  }
}
</script>

<style lang="scss">
.exchange-list {
  color: #000000;
  margin: 55px 0px 100px 0px;

  .top-title {
    margin-bottom: 46px;
  }

  .markets {
    span {
      font-weight: bold;
    }

    img {
      background: #333;
    }
  }
}
</style>
