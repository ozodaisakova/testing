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
            src: '/r-1.jpg'
          },
          {
            src: '/r-2.jpg'
          },
          {
            src: '/r-3.jpg'
          },
          {
            src: '/r-4.jpg'
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
