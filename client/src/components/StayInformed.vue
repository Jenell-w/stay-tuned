<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <div class="health-news-feed">
      <h2 @click="getLatestArticles">Click for Latest News:</h2>
    </div>
    <ul v-for="(newsItem, index) in healthNews" v-bind:key="index">
      <li>
        <div>{{ healthNews.data.results }}</div>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "StayInformed",
  props: {
    title: String
  },
  data() {
    return {
      showNewsFeed: false,
      healthNews: []
    };
  },
  methods: {
    getLatestArticles() {
      let apiKey = "u9ndSdnU5uvVbE7DqT5Dj0v0gO0QfUgO";
      axios
        .get(
          "https://api.nytimes.com/svc/news/v3/content/all/health.json?api-key=" +
            apiKey
        )
        .then(results => {
          this.healthNews = results;
          console.log(this.healthNews);
        });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
