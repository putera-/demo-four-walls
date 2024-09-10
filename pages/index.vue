<template>
    <div style="height: 100vh; position: fixed; top: 0; left: 0; right: 0; z-index: 1;">
        <v-img src="https://admin1.the-gypsy.sg/img/app/50e0a0211569743c4e12032a33e87053.jpg" aspect-ratio="16/9" cover
            :class="['zoom-effect', { 'zoomed': isZoomed }]" style="height: 100%;"></v-img>
    </div>


    <div style="min-height: 100vh; position: relative; z-index: 2; background-color: #fff; margin-top: 100vh;">
        <Residential />
        <Commertial />
    </div>
</template>

<script setup lang="ts">
const isZoomed = ref(false)

onMounted(() => {
    setTimeout(() => {
        isZoomed.value = true
    }, 100) // Small delay to ensure the transition starts after mount
})
</script>

<style scoped>
.zoom-effect {
    transition: transform 10s ease-out;
}

.zoomed {
    transform: scale(1.1);
}
</style>