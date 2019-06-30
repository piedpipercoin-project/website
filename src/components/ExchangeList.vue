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
      markets: [],
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
