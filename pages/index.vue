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
            src: 'https://ch3301files.storage.live.com/y4piQixBo51zLy_mTkN6UZ0_kPLewtSsQ1SWFOAOnWc3ciBMmUVGV82fAhyS7qXwTzQ_jFHGUlqMBy5SPf0hhZ44TtOdUEkBCIjaTNvdPAecaUIxjQGp3sln63Op1eft69JojfoTjbIJ3yhVaQGPsod-lKChx9ylcFeIa0leoV3dG1FE1HWcvI9es42VSMUxC4-/IMG_20160925_230333_603.jpg?psid=1&width=494&height=617'
          },
          {
            src: 'https://ch3302files.storage.live.com/y4p_u7HO3uyzAfXJaulJXwKq34RZM-m07WBr8FBD_0SM8CVxp62oxKiYANEXThUn2PAFxdM43kTA9zIje3X4sLke-TpvWcTCYfZXZCi_s080PceLfD3kWDTqeSc1Uq_KU9VQ_nv3lAfslUF-CA-2uJ87_cXurvjxIVNa-tUJ8jyuVvO8C_n-g3UU8_N_powqbq_/00mQRcZJlNo.jpg?psid=1&width=110&height=195'
          },
          {
            src: 'https://ch3302files.storage.live.com/y4p4YK-sBcio1BRYzdKyaauUfn0dfqxl7l6v73Rw3iLFnhhcT-8xisryV_1t2NiB2M1rf7wetYaqejgKBVNZkqSCowgSVSiUd4KOnuUu7H0L0nnlArsm5ce-4PZ4hQdHCh421E7Sk6G9cDLoJapw2_n1UoE0LUqArp2N21HuWD0NGaRzY6hP6EsqaE7Wjs1hKIB/PicsArt_1459262027427.jpg?psid=1&width=117&height=208'
          },
          {
            src: 'https://ch3301files.storage.live.com/y4p8T6iucUXtHVQjMkQqBTqxtv9sW_Smj22dY20pJo_JrS7gaNN71sl-UHjhdl88I1rxrpFotiqMnoRn8fszBhTFrMnPg3Ca5XbN6c8tysbtoBmO9mu0zL6vP0F8DJvhVIqf5JX3HnRLh98uhjrDSFJt5QT41ChWhHfO5h2ga8FCZYfRgQMgF7QjphoY0mLR62z/IMG_20151124_010006.JPG?psid=1&width=480&height=473'
          }
        ]
      }
    }
  }
</script>
<style>

.my-slider{
    box-shadow: none;
    border: none;
}
</style>
