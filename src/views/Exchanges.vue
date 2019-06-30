<template>
  <div class="exchanges">
    <b-container>
      <b-row class="justify-content-md-center">
        <b-col md="auto">
          <h1>Exchanges</h1>
        </b-col>
      </b-row>
    </b-container>

    <ExchangeList />
  </div>
</template>

<script>
import ExchangeList from '@/components/ExchangeList.vue'

export default {
  name: 'Exchanges',
  components: {
    ExchangeList
  }
}
</script>