<template>
  <v-app>
    <v-app-bar app color="#e91e63" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Sadaf"
          class="shrink mr-2"
          contain
          src="./assets/logo.png"
          transition="scale-transition"
          width="40"
        />

        <strong style="font-size:18px; margin-left:5px;"
          >Happy Birthday Rahila</strong
        >
      </div>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App'
}
</script>
