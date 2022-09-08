<template>
  <div>
    <v-img class="w-promopage" :src="backgroundUrl">
      <v-container fluid fill-height>
        <v-row>
          <v-col cols="7">
            <h2>The legend of the sun rise</h2>
          </v-col>
          <v-col cols="7">
            <p>
              <strong>
                What is Lorem Ipsum? Lorem Ipsum is simply dummy text of the printing and
                typesetting industry. Lorem Ipsum has been the industry's standard dummy
                text ever since the 1500s, when an unknown printer took a galley of type
                and scrambled it to make a type specimen book. It has survived not only
                five centuries, but also the leap into electronic typesetting, remaining
                essentially unchanged. It was popularised in the 1960s with the release of
                Letraset sheets containing Lorem Ipsum passages, and more recently with
                desktop publishing software like Aldus PageMaker including versions of
                Lorem Ipsum.</strong
              >
            </p>
          </v-col>
        </v-row>
      </v-container>
    </v-img>
    <v-container fluid class="w-trailers">
      <v-row>
        <v-col cols="12">
          <h1>Trailer</h1>
        </v-col>
        <v-col
          cols="12"
          sm="6"
          md="4"
          lg="3"
          xl="2"
          v-for="(trailer, idx) in trailers"
          :key="idx"
        >
          <Trailer :trailer="trailer"></Trailer>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid class="w-lastwatch">
      <v-row>
        <v-col cols="12">
          <h1>my last watch</h1>
        </v-col>
       <swiper class="swiper" :options="swiperOption" >
          <swiper-slide style="width: 250px !important; margin: 0px" v-for="(lastWatch, idx) in card" :key="idx"
            ><LastWatch :movie="lastWatch" />
          </swiper-slide>
        </swiper>
      </v-row>
    </v-container>
    <v-container fluid class="w-TopMovies">
      <v-row>
        <v-col cols="12">
          <h1>top movies</h1>
        </v-col>
        <v-col
          cols="12"
          sm="6"
          md="4"
          lg="3"
          xl="2"
          v-for="(topmovies, idx) in top"
          :key="idx"
        >
          <TopMovies :topMovie="topmovies" />
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid class="w-TopTv">
      <v-row>
        <v-col cols="12">
          <h1>top tv shows</h1>
        </v-col>
        <v-col
          cols="12"
          sm="6"
          md="4"
          lg="3"
          xl="2"
          v-for="(toptv, idx) in tv"
          :key="idx"
        >
          <TopTv :tvsh="toptv" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
  import 'swiper/css/swiper.css'

import TopTv from "@/components/movies/TopTv";
import TopMovies from "@/components/movies/TopMovies";
import LastWatch from "@/components/movies/LastWatch";
import Trailer from "@/components/movies/Trailer.vue";
export default {
  components: {
    Trailer,
    LastWatch,
    TopMovies,
    TopTv,
Swiper,
      SwiperSlide
  },
  data: () => ({
    backgroundUrl: require("@/assets/imgs/film.png"),
    swiperOption: {
          slidesPerView: 3,
          spaceBetween: 30,
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          }
        },
    trailers: [
      { img: require("@/assets/imgs/mo1.PNG"), index: "01" },
      { img: require("@/assets/imgs/mo2.PNG"), index: "02" },
      { img: require("@/assets/imgs/mo3.PNG"), index: "03" },
      { img: require("@/assets/imgs/mo4.PNG"), index: "04" },
    ],
    card: [
      {
        title: "Pre-fab homes",
        src:
          "https://imgc.allpostersimages.com/img/posters/top-gun-wingman_u-L-FA8JLN0.jpg",
        flex: 12,
      },

      {
        title: "Favorite road trips",
        src:
          "https://www.filmjabber.com/movie-poster-thumbs/bullet-train-movie-poster-6974.jpg",
        flex: 6,
      },
      {
        title: "Best airlines",
        src:
          "https://vibepulp.com/wp-content/uploads/2022/05/The-Gray-Man-Movie-2022-Netflix-Cast-Roles-Trailer-Story-Release-Date-Poster-819x1024.jpg",
        flex: 6,
      },
          {
        title: "Favorite road trips",
        src:
          "https://imgc.allpostersimages.com/img/posters/disney-hocus-pocus-moon_u-L-FA8O530.jpg",
        flex: 6,
      },
      {
        title: "Best airlines",
        src:
          "https://vibepulp.com/wp-content/uploads/2022/05/The-Gray-Man-Movie-2022-Netflix-Cast-Roles-Trailer-Story-Release-Date-Poster-819x1024.jpg",
        flex: 6,
      },
      {
        title: "Best airlines",
        src: "https://wallpapercave.com/wp/wp10941904.jpg",
        flex: 6,
      },
      {
        title: "Best airlines",
        src: "https://imgc.allpostersimages.com/img/posters/the-wolf-man-illustration_u-L-FA8L0P0.jpg",
        flex: 6,
      },
      {
        title: "Best airlines",
        src: "https://imgc.allpostersimages.com/img/posters/marvel-cinematic-universe-doctor-strange-portal_u-L-FA8JLM0.jpg",
        flex: 6,
      },
    ],
    top: [
      {
        title: "Pre-fab homes",
        src:
          "https://imgc.allpostersimages.com/img/posters/the-goonies-one-sheet-premium-poster_u-L-F9PHF30.jpg",
        flex: 12,
      },

      {
        title: "Favorite road trips",
        src:
          "https://imgc.allpostersimages.com/img/posters/lord-of-the-rings-1-the-fellowship-of-the-ring_u-L-F4S6EA0.jpg?artHeight=900&artPerspective=n&artWidth=900",
        flex: 6,
      },
      {
        title: "Best airlines",
        src:
          "https://imgc.allpostersimages.com/img/posters/harry-potter-and-the-philosopher-s-stone_u-L-F4S6BV0.jpg?artHeight=900&artPerspective=n&artWidth=900",
        flex: 6,
      },
      {
        title: "Best airlines",
        src: "https://i.pinimg.com/564x/0d/c1/03/0dc1036dc57409d7a5e6809c3f64517c.jpg",
        flex: 6,
      },
    ],
    tv: [
      {
        title: "Pre-fab homes",
        src: "https://i.pinimg.com/736x/e3/7e/aa/e37eaaf7ad6d8c992762e4e4c0e98c4e.jpg",
        flex: 12,
      },

      {
        title: "Favorite road trips",
        src: "https://api.time.com/wp-content/uploads/2021/12/Neil-Jamieson-TV-1.jpg",
        flex: 6,
      },
      {
        title: "Best airlines",
        src:
          "https://imgc.allpostersimages.com/img/posters/back-to-the-future-1985-directed-by-robert-zemeckis_u-L-Q1H92310.jpg",
        flex: 6,
      },
            {
        title: "Best airlines",
        src:
          "https://imgc.allpostersimages.com/img/posters/marvel-thor-love-and-thunder-thor-one-sheet_u-L-FA8JWX0.jpg",
        flex: 6,
      },
    ],
  }),

  methods: {
    //
  },
};
</script>
<style>
.w-promopage {
  height: 100vh;
  width: 100%;
  object-fit: cover;
}

.w-promopage p {
  color: black;
}

.w-trailers {
  position: relative;
  bottom: 200px;
  z-index: 2;
}
.w-lastwatch {
  position: relative;
  bottom: 200px;
  z-index: 2;
}
.w-TopMovies {
  position: relative;
  bottom: 200px;
  z-index: 2;
}
.w-TopTv {
  position: relative;
  bottom: 200px;
  z-index: 2;
}
</style>
