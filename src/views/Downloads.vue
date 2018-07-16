<template>
  <v-app>
    <v-container fluid grid-list-md style="padding-top: 75px">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 pa-2 v-for="device in devices" :key="device.id">
          <v-card hover :href="getSfLink(device.id)">
            <v-card-media height="250px" :src="getImgUrl(device.id)">
            </v-card-media>
            <v-card-title primary-title>
              <div>
                <div class="headline">{{ device.name }}</div>
                <span class="grey--text">Maintainer: {{ device.maintainer }}</span>
              </div>
            </v-card-title>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
  export default {
    name: 'Downloads',
    data () {
      return {
        devices: [
          {
            id: 'bacon',
            name: 'OnePlus One',
            maintainer: 'Kshitij Gupta (AgentFabulous)',
          },
          {
            id: 'oneplus2',
            name: 'OnePlus 2',
            maintainer: 'Shreyansh Lodha',
          },
          {
            id: 'oneplus3',
            name: 'OnePlus 3/3T',
            maintainer: 'Nico Franke (ZerNico)',
          },
          {
            id: 'dumpling',
            name: 'OnePlus 5T',
            maintainer: 'Pranav Thombare',
          },
          {
            id: 'kenzo',
            name: 'Redmi Note 3',
            maintainer: 'Absar Rahman',
          },
          {
            id: 'mido',
            name: 'Redmi Note 4',
            maintainer: 'Adesh Ikhar (Adesh15)',
          },
          {
            id: 'whyred',
            name: 'Redmi Note 5 Pro',
            maintainer: 'Devansh Bajaj (devansh23)',
          },
          {
            id: 'z2_plus',
            name: 'Zuk Z2 Plus',
            maintainer: 'Anunay Maheshwari (anunaym14)',
          },
          {
            id: 'sanders',
            name: 'Moto G5S Plus',
            maintainer: 'Keertesh',
          },
          {
            id: 'X00TD',
            name: 'Asus ZenFone Max Pro (M1)',
            maintainer: 'Akash Khatri',
          },
        ]
      }
    },
    methods: {
      getImgUrl(id) {
        return require('@/assets/phones/' + id + '.jpg')
      },
      getSfLink(id) {
        return 'https://sourceforge.net/projects/posp/files/' + id
      }
    }
  }
</script>
