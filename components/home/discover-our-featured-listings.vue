<template>
    <div>
        <div class="d-flex gap-2 justify-center ga-3 mt-12">
            <IconsOffice height="17" />
            <span>DISCOVER FEATURED</span>
        </div>
        <div class="featured-title text-h4 text-md-h3 text-center mt-6">DISCOVER OUT FEATURED LISTINGS</div>

        <div class="featured-sub-title text-center text-grey-darken-1 mt-6 text-uppercase">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa dolorem quis laudantium quas eveniet
            similique.
        </div>

        <v-row justify="center" class="my-6">
            <template v-for="(img, i) in images" :key="i">
                <v-col cols="12" md="4">
                    <v-hover v-slot:default="{ isHovering, props }">
                        <v-responsive class="rounded">
                            <!-- class="fade-in-up" -->
                            <v-img :src="img.url" cover aspect-ratio="1.3" style="height: 100%;">
                                <div v-bind="props" :style="[
                                    isHovering ? 'background-color: rgba(0, 0, 0, 0.0)' : 'background-color: rgba(0, 0, 0, 0.3)',
                                    'transition: background-color 0.3s ease'
                                ]" class="fill-height px-4 py-4 text-white font-weight-light">
                                    <div class="d-flex flex-column justify-space-between fill-height">
                                        <div>
                                            <v-badge v-if="img.featured" color="success" content="FEATURED" inline
                                                rounded="0" />
                                        </div>
                                        <div>
                                            <v-badge color="black" content="FOR RENT" inline rounded="0"
                                                class="badge-opacity" />
                                            <div class="text-h5 font-weight-bold">{{ img.price }}</div>
                                            <div
                                                class="d-flex flex-column flex-md-row justify-space-between align-center ga-3">
                                                <div class="d-flex ga-3">
                                                    <div class="d-flex ga-1 align-center">
                                                        <v-icon icon="mdi-bed-king-outline" />
                                                        <div> {{ img.facility.bed }}</div>
                                                    </div>
                                                    <div class="d-flex ga-1 align-center">
                                                        <IconsShower height="18" />
                                                        <div> {{ img.facility.shower }}</div>
                                                    </div>
                                                    <div class="d-flex ga-1 align-center">
                                                        <IconsCar height="18" />
                                                        <div> {{ img.facility.car_park }}</div>
                                                    </div>
                                                    <div class="d-flex ga-1 align-center">
                                                        <IconsRullerTriangle height="18" />
                                                        <div> {{ img.facility.area }}</div>
                                                    </div>
                                                </div>
                                                <div class="d-flex ga-1">
                                                    <v-btn density="compact" icon="mdi-arrow-expand" color="black"
                                                        class="btn-opacity rounded-sm" />
                                                    <v-btn density="compact" icon="mdi-heart-outline" color="black"
                                                        class="btn-opacity rounded-sm" />
                                                </div>
                                            </div>
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
        url: '/images/12.jpg',
        featured: true,
        price: '$4,500/mo',
        facility: {
            bed: 4,
            shower: 2,
            car_park: 1,
            area: '1200 Sq Ft'
        }
    },
    {
        url: '/images/13.jpg',
        featured: true,
        price: '$876,000',
        facility: {
            bed: 3,
            shower: 2,
            car_park: 1,
            area: '2560 Sq Ft'
        }
    },
    {
        url: '/images/14.jpg',
        featured: true,
        price: '$11,000/mo',
        facility: {
            bed: 3,
            shower: 1,
            car_park: 1,
            area: '1789 Sq Ft'
        }
    },
    {
        url: '/images/15.jpg',
        featured: false,
        price: '$5,600/mo',
        facility: {
            bed: 5,
            shower: 3,
            car_park: 1,
            area: '3450 Sq Ft'
        }
    },
    {
        url: '/images/16.jpg',
        featured: false,
        price: '$3,500/mo',
        facility: {
            bed: 1,
            shower: 1,
            car_park: 1,
            area: '1760 Sq Ft'
        }
    },
    {
        url: '/images/17.jpg',
        featured: false,
        price: '$3,750/mo',
        facility: {
            bed: 1,
            shower: 1,
            car_park: 1,
            area: '1678 Sq Ft'
        }
    }
]

</script>

<style scoped>
.badge-opacity {
    opacity: 0.6;
}

.btn-opacity {
    opacity: 0.4;
}
</style>
