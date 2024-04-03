<template>
  <v-app id="inspire">
    <v-app-bar flat>
      <v-container class="mx-auto d-flex align-center justify-center">
        <v-row>
          <v-col cols="4">
            <span>🍌 ⋆ 🍒  🎀  小蓝书  🎀  🍒 ⋆ 🍌</span>
          </v-col>
          <v-col cols="8">
           <v-responsive max-width="400">
             <v-text-field
               density="compact"
               label="搜索"
               rounded="lg"
               variant="solo-filled"
               flat
               hide-details
               single-line
               append-inner-icon="mdi-magnify"  
               @click:appendInner="handleAppendIconClick"
             ></v-text-field>
           </v-responsive>
          </v-col>
        </v-row>
      </v-container>
    </v-app-bar>

    <v-main class="bg-grey-lighten-3">
      <v-container>
        <v-row>
          <v-col cols="2">
            <v-sheet rounded="lg">
              <v-list rounded="lg">
                  <v-list-item
                    color="grey-lighten-4"
                    title="发现"
                    prepend-icon="mdi-text-search"
                    link
                    href="/search"
                  ></v-list-item>
                  <v-list-item
                    color="grey-lighten-4"
                    title="发布"
                    prepend-icon="mdi-publish"
                    link
                  ></v-list-item>
                  <v-list-item
                    color="grey-lighten-4"
                    title="通知"
                    prepend-icon="mdi-message-alert-outline"
                    link
                  ></v-list-item>


                <v-divider class="my-2"></v-divider>

                  <v-list-item
                    color="grey-lighten-4"
                    title="我"
                    prepend-icon="mdi-account-circle"
                    link
                  ></v-list-item>
              </v-list>
            </v-sheet>
          </v-col>

          <v-col>
            <v-sheet
              min-height="70vh"
              rounded="lg"
            >
              <router-view></router-view>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <AppFooter></AppFooter>
  </v-app>
</template>

<script setup>
import AppFooter from '../components/AppFooter.vue';

  const links = [
    'Dashboard',
    'Messages',
    'Profile',
    'Updates',
  ]
  const handleAppendIconClick=()=>{
    console.log("click")
  }
</script>
