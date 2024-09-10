<template>
    <v-row>
        <v-col cols="12" md="4">
            <v-row>
                <v-col>
                    <v-responsive :aspect-ratio="$vuetify.display.mdAndUp ? 1 : undefined">
                        <v-card flat class="d-flex flex-column justify-space-between fill-height">
                            <div class="d-flex flex-column justify-center align-md-center fill-height">
                                <div>
                                    <v-card-title class="text-h5 font-weight-light px-0">Residential</v-card-title>
                                    <v-card-text class="font-weight-light px-0">
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
                                        tempor
                                        incididunt
                                    </v-card-text>
                                </div>
                            </div>
                            <v-divider width="30%" opacity="1" class="mt-14 mt-md-0"></v-divider>
                        </v-card>
                    </v-responsive>
                </v-col>
            </v-row>
            <v-row>
                <v-col>
                    <GridCard image="/images/1.jpg" properties_name="Apartment" properties_count="23" />
                </v-col>
            </v-row>
        </v-col>

        <v-col cols="12" md="4" class="d-flex flex-column">
            <GridCard image="/images/2.jpg" properties_name="Studio" properties_count="7" />
        </v-col>

        <v-col cols="12" md="4">
            <v-row>
                <v-col>
                    <GridCard image="/images/3.jpg" properties_name="Single Family Home" properties_count="12" />
                </v-col>
            </v-row>
            <v-row>
                <v-col>
                    <GridCard image="/images/4.jpg" properties_name="Villa" properties_count="12" />
                </v-col>
            </v-row>
        </v-col>
    </v-row>
</template>