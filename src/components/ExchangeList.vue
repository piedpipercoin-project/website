<template>
  <div class="exchange-list">
    <b-container>
      <b-row>
        <b-col v-if="markets" class="mt-3">
          <b-card-group deck class="markets">
              <b-card
                :title="market.name"
                :img-src="market.logo"
                img-alt="Image"
                img-top
                tag="article"
                class="mb-3"
                style="min-width: 210px;"
                v-for="market in markets" :key="market.pair"
              >
                <!-- <b-card-text>
                  Some quick example text to build on the card title and make up the bulk of the card's content.
                </b-card-text> -->

                <div class="text-center">
                  <b-button size="sm" :href="market.link" variant="primary" target="_blank">Visit Exchange</b-button>
                </div>
              </b-card>
          </b-card-group>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'ExchangeList',
  data: function() {
    return  {
      markets: [
        { name: "ForkDelta", price: 0.00002587, pair: "PPI-BTC", link: "https://forkdelta.app/#!/trade/0x5a3c9a1725aa82690ee0959c89abe96fd1b527ee-ETH", logo: "https://piedpipercoin.com/img/forkdelta.5f02e8db.png" },
        { name: "DDEX", price: 0.00002587, pair: "PPI-BTC", link: "https://ddex.io/trade/PPI-WETH", logo: "https://www.piedpipercoin.com/img/ddex.16f3e602.png" },
        { name: "CryptoBridge", price: 0.00002587, pair: "PPI-BTC", link: "https://wallet.crypto-bridge.org/market/BRIDGE.PPI_BRIDGE.BTC", logo: "https://www.piedpipercoin.com/img/cryptobridge.d9310f9d.png" },
        { name: "IDAX", price: 0.00002587, pair: "PPI-BTC", link: "https://www.idax.pro/exchange?pairname=PPI_BTC", logo: "https://www.piedpipercoin.com/img/cryptobridge.d9310f9d.png" },
        { name: "Saturn Network", price: 0.00002587, pair: "PPI-BTC", link: "https://www.saturn.network/exchange/ETH/order-book/0x5a3c9a1725aa82690ee0959c89abe96fd1b527ee/0x0000000000000000000000000000000000000000", logo: "https://www.piedpipercoin.com/img/saturn%20network.759cbcdd.png" },
        { name: "bamboorelay", price: 0.00002587, pair: "PPI-BTC", link: "https://bamboorelay.com/trade/PPI-WETH", logo: "https://www.piedpipercoin.com/img/cryptobridge.d9310f9d.png" }
      ]
    }
  }
}
</script>

<style lang="scss">
.exchange-list {
  color: #000000;
  margin: 55px 0px 0px 0px;

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
