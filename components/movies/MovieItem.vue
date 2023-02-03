<template>
  <!-- 
    class="col-lg-3 col-md-4 col-sm-6" 

style="display:flex; justify-content: center; flex-wrap: wrap;"
  -->
  <div class="berjejer">
    <div v-for="(movie, index) in movieData" :key="index">
      <div class="featured__item"  >
          <img
          class="featured__item__pic"
          :src="movie.link"
          />
          <nuxt-link tag="h5" class="featured__item__text" :to="{name: 'detail', params: {detail: movie}}">
            {{ movie.name }}
          </nuxt-link>
        </div>
      </div>
    </div>
  </template>
<script> 
export default {
  data() {
    return {
      movieData: [
        {
          name: "Avatar: The Way of Water",
          link: "https://i.ibb.co/PjB95Lr/movie1.jpg",
          genre: "Science Fiction",
          year: 2022,
          review: "Avatar: The Way of Water",
        },
        {
          name: "Insidious 1",
          link: "https://i.ibb.co/vh30y4P/movie2.jpg",
          genre: "Horror",
          year: 2010,
          review: "Insidious 1",
        },
        {
          name: "Jumanji: The Next Level",
          link: "https://i.ibb.co/SKjMVJK/movie5.jpg",
          genre: "Adventure",
          year: 2019,
          review: "Jumanji: The Next Level",
        },
        {
          name: "Avengers: Infinity War",
          link: "https://i.ibb.co/Tg5rkBj/movie6.jpg",
          genre: "Action",
          year: 2018,
          review: "Avengers: Infinity War",
        },
        {
          name: "Avengers: Infinity War",
          link: "https://i.ibb.co/Tg5rkBj/movie6.jpg",
          genre: "Action",
          year: 2018,
          review: "Avengers: Infinity War",
        },
        {
          name: "Avengers: Infinity War",
          link: "https://i.ibb.co/Tg5rkBj/movie6.jpg",
          genre: "Action",
          year: 2018,
          review: "Avengers: Infinity War",
        },
      ],
    };
  }
}
</script>
<style scoped>

.berjejer{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.featured__item {
  margin-bottom: 50px;
  margin-left: 20px;
  margin-right: 20px;
  margin-top: 20px;
  display: grid;

}

.featured__item__pic {
  height: 330px;
  width: 270px;
  position: relative;
  overflow: hidden;
  background-position: center center;
}

.featured__item__text {
  text-align: center;
  padding-top: 15px;
}

.featured__item__text h6 {
  margin-bottom: 10px;
}

.featured__item__text h6 a {
  color: #252525;
}

.featured__item__text h5 {
  color: #252525;
  font-weight: 700;
}
</style>