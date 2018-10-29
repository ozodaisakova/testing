<template>
  <v-carousel hide-delimiters  class="my-slider">
    <v-carousel-item 
        v-for="(item,i) in items"
        :key="i">
      <v-layout row wrap align-center fill-height >
        <v-flex>
            <v-img
              :src="item.src"
              :lazy-src="`https://picsum.photos/10/6?image=15`"  
              fill-height>
            <v-layout
              slot="placeholder"
              fill-height
              align-center
              justify-center
              ma-0>
              <v-progress-circular indeterminate color="grey"></v-progress-circular>
            </v-layout> 
          </v-img>
        </v-flex>
      </v-layout>      
    </v-carousel-item>
  </v-carousel>
</template>
<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://db3pap001files.storage.live.com/y4p8rwhEJKVg1eYXMFumv3MOqQG7UAOt-Vsk7K6fgkKhw6jRy_Osc4tFtMz6aaLl9jLBJIt7ne9Gz1-9rwP2rb1nBFf_QVS6p52XWQDNXNCa17P-CMowqUzVvQMSDqBgQesRyVNJxcB2OfB6kB2pb7mNmA8vvWX24jMvgtY1rmGeFp8mkxtmBBjhEEWOQR3B2aF/IMG-20160122-WA0004.jpg?psid=1&width=463&height=617'
          },
          {
            src: 'https://db3pap001files.storage.live.com/y4pdIWDqxzmIMm92yWrsSvAtqOTCF3gDQtRTV7LW9MqgCSg-sQtHDTlF_nQz8Bm2CuR04Md1V4th26i-2bY_5OI77FM8W59ROjq8wsf4Y6Bx7uqaOrywTo3uBdzj7MujzhiKgxF0SjYP_N578x3E3xbZm0DtPbwzQRMRTxhOcshjOlFpegV92Af3yJlZB8PKgTg/2016-09-13-17-46-08-270.jpg?psid=1&width=463&height=617'
          },
          {
            src: 'https://db3pap001files.storage.live.com/y4p91RX5LF22v0nECijGCZEVmJH6HtDV9ae60nOxN2J0xGWQygt3967X8CzVg3ni-CcEsaxtzpKL9wIHf5PXt73LqskUxbaB-Bl_HVHuoNjoNc8m8eJNIOBwVPmM1Pw4eEt7OAmqdpZgX6m7uv-sQVPbDn3LhdQ95QCw38RzNXoKcQ_C07J00PnDaEBB0wokEMU/2016-09-18-16-47-03-199.jpg?psid=1&width=463&height=617'
          },
          {
            src: 'https://db3pap001files.storage.live.com/y4ph25nlAh3VzICp6srL8QO9JGLMPnasIgUrUoH_lTYXU3j1R2wF2Vvo_UDh2dFU5nnDk_-cpOh-JOhgZxPsDlXDE7J1puRYkLxfIB2qGkxXR99hm4GR44kZT2BuT4D7ld0uN95ixLJA2YOkxxBkI7lP44qbwjXNeoNPc-r-W0mtYW6yEqpumkW1bHIXK9oo7MY/2016-11-24-16-43-50-304.jpg?psid=1&width=463&height=617'
          }
        ]
      }
    }
  }
</script>
<style scoped>

.my-slider{
    box-shadow: none;
    border: none;
}
</style>
