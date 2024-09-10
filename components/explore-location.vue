<template>
  <div>
    <div class="d-flex gap-2 justify-center ga-3 mt-12">
      <IconsOffice height="17" />
      <span>EXPLORE LOCATION</span>
    </div>
    <div class="featured-title text-h4 text-md-h3 text-center mt-6">“Discover the Best Locations around the Globe</div>

    <div class="featured-sub-title text-center text-grey-darken-1 mt-6">
      EXPLORE DIVERSE NEIGHBORHOODS, EACH OFFERING UNIQUE AMENITIES AND LIFESTYLE OPPORTUNITIES.
    </div>

    <v-row justify="center" class="my-6">
      <template v-for="(img, i) in images" :key="i">
        <v-col cols="12" md="4">
          <v-hover v-slot:default="{ isHovering, props }">
            <v-responsive class="rounded">
              <v-img :src="img.url" cover aspect-ratio="0.75" style="height: 100%;" class="fade-in-up">
                <div v-bind="props" :style="[
                  isHovering ? 'background-color: rgba(0, 0, 0, 0.0)' : 'background-color: rgba(0, 0, 0, 0.3)',
                  'transition: background-color 0.3s ease'
                ]" class="fill-height px-8 py-8 text-white font-weight-light">
                  <div class="d-flex flex-column justify-end fill-height">
                    <div class="d-flex flex-column flex-md-row justify-space-between align-center ga-3">
                      <div class="font-weight-light text-center text-md-left">
                        <div>{{ img.properties_count }} Properties</div>
                        <div class="text-h4 font-weight-bold text-white">{{ img.title }}</div>
                      </div>
                      <v-btn color="red-darken-2">VIEW</v-btn>
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
    title: "GOA",
    url: '/images/9.jpg',
    properties_count: 24,
  },
  {
    title: "BATAM",
    url: '/images/10.jpg',
    properties_count: 14,
  },
  {
    title: "MUMBAY",
    url: '/images/11.jpg',
    properties_count: 14,
  }
]

</script>
