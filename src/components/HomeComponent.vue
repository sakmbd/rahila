<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <video width="100%" controls>
          <source src="@/assets/video.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col cols="12">
        <v-card class="mx-auto" max-width="400">
          <v-img
            class="white--text align-end"
            height="400x"
            src="/photos/Rahila_Rehman (60).jpg"
          >
          </v-img>
          <v-card-text class="pink darken-1">
            <div class="white--text">
              May Allah shower Good Luck from up above the heaven and make you the luckiest in this world. May Allah shower his countless blessings on you and your family.
              <br/>Happy Birthday Rahila Rehman!
            </div>
          </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12">
        <v-card class="mx-auto" max-width="400">
          <v-img
            class="white--text align-end"
            height="400px"
            src="/photos/Rahila_Rehman (56).jpg"
          >
            <v-card-title class="pink"
              >Happy Birthday Rahila Rehman</v-card-title
            >
          </v-img>
        </v-card>
      </v-col>

      <v-col cols="12">
        <v-card class="mx-auto" color="#26c6da" dark max-width="400">
          <v-card-title>
            <v-icon large left>
              mdi-twitter
            </v-icon>
            <span class="title font-weight-light font-weight-bold"
              >Happy Birthday Rahila</span
            >
          </v-card-title>

          <v-card-text class="headline font-weight-bold">
            "You are the sweetest person I know, and this birthday is a fresh beginning. I wish you confidence, courage, and capability. Happy birthday."
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row class="text-center">
      <v-col cols="12">
        <v-card class="mx-auto gallery" dark max-width="400">
          <v-card-title>
            <v-icon large left class="black--text">
              mdi-camera
            </v-icon>
            <span class="title font-weight-light font-weight-bold black--text" >Photos Gallery</span>
          </v-card-title>
          <CoolLightBox :items="images" :index="index" @close="index = null">
          </CoolLightBox>
          <v-row class="images-wrapper">
            <v-col cols="4"
              class="image"
              v-for="(image, imageIndex) in images"
              :key="imageIndex"
              @click="index = imageIndex"
              :style="{ backgroundImage: 'url(\'' + image + '\')' }"
            ></v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
    <br><br>
  </v-container>
</template>

<script>
import CoolLightBox from 'vue-cool-lightbox'
import 'vue-cool-lightbox/dist/vue-cool-lightbox.min.css'
export default {
  components: {
    CoolLightBox
  },
  data () {
    return {
      images: [
        '/photos/1 (1).jpg',
        '/photos/1 (2).jpg',
        '/photos/1 (3).jpg',
        '/photos/1 (4).jpg',
        '/photos/1 (5).jpg',
        '/photos/1 (6).jpg',
        '/photos/1 (7).jpg',
        '/photos/1 (8).jpg',
        '/photos/1 (9).jpg',
        '/photos/1 (10).jpg',
        '/photos/1 (11).jpg',
        '/photos/1 (12).jpg',
        '/photos/1 (13).jpg',
        '/photos/1 (14).jpg',
        '/photos/1 (15).jpg',
        '/photos/1 (16).jpg',
        '/photos/1 (17).jpg',
        '/photos/1 (18).jpg',
        '/photos/1 (19).jpg',
        '/photos/1 (20).jpg',
        '/photos/1 (21).jpg',
        '/photos/1 (22).jpg',
        '/photos/1 (23).jpg',
        '/photos/1 (24).jpg',
        '/photos/1 (25).jpg',
        '/photos/1 (26).jpg',
        '/photos/1 (27).jpg',
        '/photos/1 (28).jpg',
        '/photos/1 (29).jpg',
        '/photos/1 (30).jpg',
        '/photos/1 (31).jpg',
        '/photos/1 (32).jpg',
        '/photos/1 (33).jpg',
        '/photos/1 (34).jpg',
        '/photos/1 (35).jpg',
        '/photos/1 (36).jpg',
        '/photos/1 (37).jpg',
        '/photos/1 (38).jpg',
        '/photos/1 (39).jpg',
        '/photos/1 (40).jpg',
        '/photos/1 (41).jpg',
        '/photos/1 (42).jpg',
        '/photos/1 (43).jpg',
        '/photos/1 (44).jpg',
        '/photos/1 (45).jpg',
        '/photos/1 (46).jpg',
        '/photos/1 (47).jpg',
        '/photos/1 (48).jpg',
        '/photos/1 (49).jpg',
        '/photos/1 (50).jpg',
        '/photos/1 (51).jpg',
        '/photos/1 (52).jpg',
        '/photos/1 (53).jpg',
        '/photos/1 (54).jpg',
        '/photos/1 (55).jpg',
        '/photos/1 (56).jpg',
        '/photos/1 (57).jpg',
        '/photos/1 (58).jpg',
        '/photos/1 (59).jpg',
        '/photos/1 (60).jpg',
        '/photos/1 (61).jpg',
        '/photos/1 (62).jpg'
      ],
      index: null
    }
  }
}
</script>

<style>
/* .images-wrapper {
  display: flex;
} */
.image {
  height: 100px;
  width: 200px;
  margin: 30px;
}
.gallery {
  background: url(https://2.bp.blogspot.com/-Hm3T7xvyEHY/VVFzNTane3I/AAAAAAAANEU/5u8UrSAC26Y/s1600/body.png.);
}
</style>
