<template>
    <v-container class="mx-auto" style="max-width: 1200px; ">
        <v-row class="mx-16">
            <v-col cols="12" md="4">
                <v-responsive :aspect-ratio="$vuetify.display.mdAndUp ? 1 : undefined">
                    <v-card flat class="d-flex flex-column justify-center align-md-center fill-height">
                        <div>
                            <v-card-title class="text-h5 font-weight-light px-0">Commercial</v-card-title>
                            <v-card-text class="font-weight-light px-0">
                                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
                                tempor
                                incididunt
                            </v-card-text>
                        </div>
                    </v-card>
                </v-responsive>
            </v-col>
            <v-col cols="12" md="4">
                <GridCard image="/images/5.jpg" properties_name="Office" properties_count="3" />
            </v-col>
            <v-col cols="12" md="4">
                <GridCard image="/images/6.jpg" properties_name="Shop" properties_count="3" />
            </v-col>
        </v-row>
    </v-container>
</template>

<script setup lang="ts">

</script>

<style scoped></style>