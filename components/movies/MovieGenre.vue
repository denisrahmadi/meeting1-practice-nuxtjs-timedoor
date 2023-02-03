<template>
  <div>
    <div class="featured__controls">
      <ul>
        <li @click="filterCategoryMovie('')">All</li>
        <li @click="filterCategoryMovie('Actions')">Actions</li>
        <li @click="filterCategoryMovie('Science Fiction')">Science Fiction</li>
        <li @click="filterCategoryMovie('Horror')">Horror</li>
        <li @click="filterCategoryMovie('Thriller')">Thriller</li>
        <li @click="filterCategoryMovie('Comedy')">Comedy</li>
        <li @click="filterCategoryMovie('Romance')">Romance</li>
        <li @click="filterCategoryMovie('Adventure')">Adventure</li>
        <li @click="filterCategoryMovie('Fantasy')">Fantasy</li>
      </ul>
      {{ filterCategory }}
    </div>
  </div>
</template>
<script>
import { X509Certificate } from 'crypto';

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
      filterCategory: ''
    };
  },
  methods: {
    filterCategoryMovie(category) {
      this.filterCategory = category
      this.movieData.map((e) => {
        e.filter((i) => {
          if (i.genre == category) {
            return 
          }
        })
      })

    },
  },
};
</script>
<style scoped>
.featured__controls {
  text-align: center;
  margin-bottom: 50px;
}

.featured__controls ul li {
  list-style: none;
  font-size: 18px;
  color: #1c1c1c;
  display: inline-block;
  margin-right: 25px;
  position: relative;
  cursor: pointer;
}

.featured__controls ul li.active:after {
  opacity: 1;
}

.featured__controls ul li:after {
  position: absolute;
  left: 0;
  bottom: -2px;
  width: 100%;
  height: 2px;
  background: #7fad39;
  content: "";
  opacity: 0;
}

.featured__controls ul li:last-child {
  margin-right: 0;
}
</style>
