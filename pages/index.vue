<template>
    <div style="height: 100vh; position: fixed; top: 0; left: 0; right: 0; z-index: 1;">
        <v-img src="https://admin1.the-gypsy.sg/img/app/50e0a0211569743c4e12032a33e87053.jpg" aspect-ratio="16/9" cover
            :class="['zoom-effect', { 'zoomed': isZoomed }]" style="height: 100%;"></v-img>
    </div>


    <div style="min-height: 100vh; position: relative; z-index: 2; background-color: #fff; margin-top: 100vh;">
        <v-container class="mx-auto px-4 medium:px-16" style="max-width: 1200px; ">
            <FeaturedOption />
            <Residential />
            <Commertial />
            <ExploreLocation />
            <HomeDiscoverOurFeaturedListings />
            <ExplorePartnering />
        </v-container>
    </div>
</template>

<script setup lang="ts">
const isZoomed = ref(false)

onMounted(() => {
    setTimeout(() => {
        isZoomed.value = true
    }, 100) // Small delay to ensure the transition starts after mount
});

const handleIntersection = (entries, observer) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('visible')
            observer.unobserve(entry.target)
        }
    })
}

onMounted(() => {
    const observer = new IntersectionObserver(handleIntersection, {
        threshold: 0.1, // Trigger when 10% of the element is visible
    })

    const cards = document.querySelectorAll('.fade-in-up')
    cards.forEach(card => {
        observer.observe(card)
    })
})
</script>

<style>
.zoom-effect {
    transition: transform 10s ease-out;
}

.zoomed {
    transform: scale(1.1);
}

.fade-in-up {
    opacity: 0;
    transform: translateY(200px);
    transition: opacity 2s ease, transform 2s ease;
}

.fade-in-up.visible {
    opacity: 1;
    transform: translateY(0);
}

.featured-title {
    font-family: 'DM Serif Display';
}

.featured-sub-title {
    letter-spacing: 5px;
}
</style>
