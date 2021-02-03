<template>
    <v-card outlined color="#385F73" class="mx-auto my-auto" width="80vw" height="80vh">
        <v-container fluid fill-height>
            <v-row>
            <!--                        MENU                     -->
                <v-col cols=2 align-self="center">
                    <v-card-actions>
                        <v-navigation-drawer color="#385F73" dark style="height: 70vh">
                            <v-list
                                nav
                            >
                                <v-list-item
                                    v-for="item in menuItems"
                                    :key="item.label"
                                    link
                                >
                                    <v-list-item-icon>
                                        <v-icon>{{ item.icon }}</v-icon>
                                    </v-list-item-icon>
                                    <v-list-item-content>
                                        <v-list-item-title>{{ item.label }}</v-list-item-title>
                                    </v-list-item-content>
                                </v-list-item>
                            </v-list>
                        </v-navigation-drawer>
                    </v-card-actions>
                </v-col>
                <!-- <v-divider/> -->
            <!--                        OPTIONS                     -->
                <v-col cols=3 align-self="center">
                    <v-card-text>
                        <div> TEST </div>
                    </v-card-text>
                </v-col>
            <!--                        MAP                     -->
                <v-col cols=6 align-self="center">
                    <div id="map">
                        <mapbox
                            access-token="pk.eyJ1IjoicGlua3RydWNrIiwiYSI6ImNrMTU3M3FpZzBwaXEzbnFqNmh2anFhdjUifQ.fSS505uL0Zn-SlQoUglO8w"
                            :map-options="{
                                style: 'mapbox://styles/mapbox/light-v9',
                                center: [-96, 37.8],
                                zoom: 3,
                            }"
                            />
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>

<script>
import Mapbox from 'mapbox-gl-vue'

export default {
  name: 'MapCreator',
  components: { Mapbox },
  data: () => ({
    menuItems: [
      { label: 'Locatie', icon: 'mdi-map-marker' },
      { label: 'Stijlen', icon: 'mdi-palette' },
      { label: 'Tekst', icon: 'mdi-format-color-text' }
    ]
  }),
  methods: {
  }
}
</script>

<style>
#map {
  width: 100%;
  height: 500px;
}
</style>
