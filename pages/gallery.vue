<template>
  <div class="container">
    <div v-for="piece in gallery" :key="piece.title" class="row">
      <div class="col-xl-12">
        <h1 class="art-title">{{ piece.title }}</h1>
        <p class="art-price">{{ piece.price }}</p>
        <img class="art-container" :src="piece.image"/>
        <div id="art-footer">
          <p>{{ piece.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  data: function() {
    let gallery = {gallery: [
      {
        title: 'TitleGoesHere1',
        price: '$69',
        image: '1.jpg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'TitleGoesHere2',
        price: '$69',
        image: 'assets/images/2.jpg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'TitleGoesHere3',
        price: '$69',
        image: 'assets/images/3.jpg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'TitleGoesHere4',
        price: '$69',
        image: 'assets/images/4.jpg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'TitleGoesHere5',
        price: '$69',
        image: 'assets/images/5.jpg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
    ]};
    return gallery;
  },
})
</script>
<style>
.art-title {
  position: left;
  left: 20px;
  padding: 0;
  margin: 0;
  float: left;
  line-height: 0.7;
}

.art-price {
  color: #858585;
  margin-top: 5px;
  font-size: 20px;
  margin-bottom: 0px;
}

.art-container {
  height: 40%;
  width: 40%;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: left;
  text-align: left;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
