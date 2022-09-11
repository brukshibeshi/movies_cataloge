<template>
  <div>
    <v-img class="w-promopage" :src="backgroundUrl">
      <v-container fluid fill-height>
        <v-row>
          <v-col cols="7">
            <h1>The legend of the sun rise</h1>
          </v-col>
          <v-col cols="7">
            <p>
              <strong>
                What is Lorem Ipsum? Lorem Ipsum is simply dummy text of 
                the printing andtypesetting industry. Lorem Ipsum has been 
                the industry's standard dummytext ever since the 1500s, </strong
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
          <h1>My last Watch</h1>
        </v-col>
        <v-col
          cols="12"
          sm="6"
          :md="idx > 0 ? '4' : '8'"
          v-for="(LastWatch, idx) in card"
          :key="idx"
        >
          <LastWatch :movie="LastWatch" />
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid class="w-TopMovies">
      <v-row>
        <v-col cols="12">
          <h1>Top movies</h1>
        </v-col>
        <v-col
          cols="12"
          sm="6"
          :md="idx > 0 ? '4' : '8'"
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
          <h1>Top Tv shows</h1>
        </v-col>
        <v-col
          cols="12"
          sm="6"
          :md="idx > 0 ? '4' : '8'"
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
  },
  data: () => ({
    backgroundUrl: require("@/assets/imgs/film.jpg"),
    swiperOption: {
      slidesPerView: 3,
      spaceBetween: 30,
      pagination: {
        el: ".swiper-pagination",
        clickable: true,
      },
    },
    trailers: [
      { img: require("@/assets/imgs/mo10.PNG"),index:"01" },
      { img: require("@/assets/imgs/mo7.PNG"), index: "02" },
      { img: require("@/assets/imgs/mo9.PNG"), index: "03" },
      { img: require("@/assets/imgs/mo11.PNG"), index: "04" },
    ],
    card: [
      {
        src:
          "https://c4.wallpaperflare.com/wallpaper/221/116/854/joaquin-phoenix-joker-batman-fire-car-hd-wallpaper-thumb.jpg",
      },

      {
        src:
          "https://www.filmjabber.com/movie-poster-thumbs/bullet-train-movie-poster-6974.jpg",
      },
      {
        src:
          "https://vibepulp.com/wp-content/uploads/2022/05/The-Gray-Man-Movie-2022-Netflix-Cast-Roles-Trailer-Story-Release-Date-Poster-819x1024.jpg",
      },
      {
        src:
          "https://imgc.allpostersimages.com/img/posters/disney-hocus-pocus-moon_u-L-FA8O530.jpg",
        flex: 6,
      },
      {
        src:
          "https://vibepulp.com/wp-content/uploads/2022/05/The-Gray-Man-Movie-2022-Netflix-Cast-Roles-Trailer-Story-Release-Date-Poster-819x1024.jpg",
      },
    ],
    top: [
      {
        src:
          "https://nypost.com/wp-content/uploads/sites/2/2022/02/box-office-210219.jpg?quality=75&strip=all",
      },

      {
        src:
          "https://imgc.allpostersimages.com/img/posters/lord-of-the-rings-1-the-fellowship-of-the-ring_u-L-F4S6EA0.jpg?artHeight=900&artPerspective=n&artWidth=900",
      },
      {
        src:
          "https://imgc.allpostersimages.com/img/posters/harry-potter-and-the-philosopher-s-stone_u-L-F4S6BV0.jpg?artHeight=900&artPerspective=n&artWidth=900",
      },
      {
        src: "https://i.pinimg.com/564x/0d/c1/03/0dc1036dc57409d7a5e6809c3f64517c.jpg",
      },
      {
        src: "https://i.pinimg.com/564x/0d/c1/03/0dc1036dc57409d7a5e6809c3f64517c.jpg",
      },
    ],
    tv: [
      {
        src:
          "https://static1.colliderimages.com/wordpress/wp-content/uploads/2021/11/Movies-Like-Lord-of-the-Rings.jpg",
      },

      {
        src: "https://api.time.com/wp-content/uploads/2021/12/Neil-Jamieson-TV-1.jpg",
      },
      {
        src:
          "https://imgc.allpostersimages.com/img/posters/back-to-the-future-1985-directed-by-robert-zemeckis_u-L-Q1H92310.jpg",
      },
      {
        src:
          "https://imgc.allpostersimages.com/img/posters/marvel-thor-love-and-thunder-thor-one-sheet_u-L-FA8JWX0.jpg",
      },
      {
        src:
          "https://cdn.cinematerial.com/p/297x/xfcznadk/hot-seat-south-african-movie-poster-md.jpg?v=1655775650",
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
  color: rgb(253, 245, 245);
  position: left;
  border: 50px;
}
.w-promopage h1 {
  color: rgb(253, 245, 245);
  position: left;

}

.w-trailers {
  position: relative;
  bottom: 350px;
  border: 50px solid transparent;
  padding: 30px;
  z-index: 100;
}
.w-trailers h1 {
  color: rgb(253, 245, 245);
}
.w-trailersidx {
  position:bottom ;
}
.w-lastwatch {
  position: relative;
  background-color: #111113;
  bottom: 400px;
  border: 50px solid transparent;
  padding: 30px;
  z-index: 2;
}
.w-lastwatch h1 {
  size: 10px;
  color: rgb(253, 245, 245);
}
.w-TopMovies {
  position: relative;
  background-color: #111113;
  bottom: 450px;
  border: 50px solid transparent;
  padding: 30px;
  z-index: 2;
}
.w-TopMovies h1 {
  color: rgb(253, 245, 245);
}
.w-TopTv {
  position: relative;
  background-color: #111113;
  bottom: 450px;
  border: 50px solid transparent;
  padding: 25px;
}
.w-TopTv h1 {
  color: rgb(253, 245, 245);
}
</style>
