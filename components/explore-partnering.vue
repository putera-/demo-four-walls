<template>
  <div>
    <div class="d-flex gap-2 justify-center ga-3 mt-12">
      <IconsOffice height="17" />
      <span>EXPLORE PARTNERING</span>
    </div>
    <div class="featured-title text-h4 text-md-h3 text-center mt-6">Become Our Partner</div>

    <div class="featured-sub-title text-center text-grey-darken-1 mt-6">
      EXPLORE DIVERSE NEIGHBORHOODS, EACH OFFERING UNIQUE AMENITIES AND LIFESTYLE OPPORTUNITIES.
    </div>

    <v-row justify="center" class="my-6">
      <template v-for="(p, i) in partners" :key="i">
        <v-col cols="12" md="4">
          <v-hover v-slot:default="{ isHovering, props }">
            <v-responsive aspect-ratio="1.2">
              <div class="d-flex flex-column justify-space-between align-center fill-height fade-in-up">
                <IconsUsers height="70" class="mx-auto" />
                <div class="text-h6">{{ p.title }}</div>
                <div class="text-center">{{ p.subtitle }}</div>
                <v-btn color="red-darken-2" min-width="200">{{ p.action }}</v-btn>
              </div>
            </v-responsive>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </div>
</template>

<script lang="ts" setup>

const partners = [
  {
    title: "Qualified Agents",
    subtitle: "Are you a Real Estate Agent. Do you want to Sell or Rent your clients property through us .",
    action: "Partner with us",
    icon: 'icons-users'
  },
  {
    title: "As a Property Developer",
    subtitle: "Do your have a property to buy or sell . We will help you find a reliable Tenant / Buyer.",
    action: "Enquire Now"
  },
  {
    title: "As an Owner",
    subtitle: "Do your have a property to buy or sell . We will help you find a reliable Tenant / Buyer.",
    action: "List Now"
  }
]

</script>
