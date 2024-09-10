<template>
  <v-hover v-slot:default="{ isHovering, props }">
    <v-responsive class="rounded">
      <v-img :src="image" cover aspect-ratio="1" style="height: 100%;" class="fade-in-up">
        <div v-bind="props" :style="[
          isHovering ? 'background-color: rgba(0, 0, 0, 0.0)' : 'background-color: rgba(0, 0, 0, 0.3)',
          'transition: background-color 0.3s ease'
        ]" class="fill-height px-8 py-8 text-white font-weight-light">
          <div class="d-flex flex-column justify-space-between fill-height">
            <div>
              <div class="text-caption">{{ properties_count }} Properties</div>
              <div class="text-h6 font-weight-light">{{ properties_name }}</div>
            </div>

            <div class="d-flex flex-row justify-space-between">
              <div class="text-caption font-weight-light">MORE DETAILS</div>
              <IconsPlay height="18" />
            </div>
          </div>
        </div>
      </v-img>
    </v-responsive>
  </v-hover>
</template>

<script lang="ts" setup>
defineProps<{
  image: String
  properties_name: String
  properties_count: String
}>();
</script>