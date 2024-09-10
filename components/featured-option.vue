<template>
  <div>
    <div class="d-flex gap-2 justify-center ga-3">
      <IconsOffice height="17" />
      <span>FEATURED OPTIONS</span>
    </div>
    <div class="featured-title text-h3 text-center mt-6">Our New Homes For Sale and Rent</div>
    <div class="featured-sub-title text-center text-grey-darken-1 mt-6">OUR PORTFOLIO INCLUDES
      HIGH-QUALITY
      VILLAS, SPACIOUS
      APARTMENTS,
      AND THOUGHTFULLY
      DESIGNED
      TOWNHOUSES.</div>

    <v-row justify="center" class="my-6">
      <template v-for="(img, i) in images" :key="i">
        <v-col cols="12" md="5">
          <v-hover v-slot:default="{ isHovering, props }">
            <v-responsive class="rounded fade-in-up">
              <v-img :src="img.url" cover aspect-ratio="9/16" style="height: 100%;">
                <div v-bind="props" :style="[
                  isHovering ? 'background-color: rgba(0, 0, 0, 0.0)' : 'background-color: rgba(0, 0, 0, 0.3)',
                  'transition: background-color 0.3s ease'
                ]" class="fill-height px-8 py-8 text-white font-weight-light">
                  <div class="d-flex flex-column justify-space-between fill-height">
                    <div class="text-center font-weight-bold">
                      <div class="text-h2 font-weight-bold text-white">{{ img.title }}</div>
                      <div>{{ img.properties_count }} Properties</div>
                    </div>
                  </div>
                </div>
              </v-img>
            </v-responsive>
          </v-hover>
        </v-col>
      </template>
    </v-row>

  </div>
</template>

<script lang="ts" setup>

const images = [
  {
    title: "BUY",
    url: '/images/7.jpg',
    properties_count: 24,
  },
  {
    title: "RENT",
    url: '/images/8.jpg',
    properties_count: 14,
  }
]

</script>

<style scoped>
.featured-title {
  font-family: 'DM Serif Display';
}

.featured-sub-title {
  letter-spacing: 5px;
}
</style>