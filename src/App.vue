<template>
  <v-app>
    <v-main>
      <v-container fluid fill-height>
        <MapCreator/>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import MapCreator from './components/MapCreator';

export default {
  name: 'App',
  components: {
    MapCreator,
  },

  // data: () => ({
  //   menuItems: [
  //     { label: 'Locatie', icon: 'mdi-map-marker' },
  //     { label: 'Stijlen', icon: 'mdi-palette' },
  //     { label: 'Tekst', icon: 'mdi-format-color-text' }
  //   ]
  // }),
};
</script>
