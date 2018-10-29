<template>
<v-carousel 
      hide-delimiters  
      class="my-slider"
      prev-icon="mdi-arrow-left-drop-circle"
      next-icon="mdi-arrow-right-drop-circle">
 <v-carousel-item 
        v-for="(item,i) in items"
        :key="i">
      <v-layout row wrap align-center fill-height >
        <v-flex>
            <v-img
              :src="item.src"
              fill-height>
            <v-layout
              slot="placeholder"
              fill-height
              align-center
              justify-center
              ma-0>
              <v-progress-circular indeterminate color="black"></v-progress-circular>
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
            src: '/o-1.jpg'
          },
          {
            src: '/o-2.jpg'
          },
          {
            src: '/o-3.jpg'
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
