<template>
  <div class="container">
    <div v-for="piece in gallery" :key="piece.title">
      <div>
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
        title: 'Black Lines of Destiny',
        price: '$69',
        image: 'https://i.imgur.com/JAGwIrL.jpg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Black, white + Green',
        price: '$69',
        image: 'https://i.imgur.com/wIVFNMz.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Colours of the void',
        price: '$69',
        image: 'https://i.imgur.com/3TjJZRa.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Dimensions 1',
        price: '$69',
        image: 'https://i.imgur.com/iGOU7vU.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Dimensions 2',
        price: '$69',
        image: 'https://i.imgur.com/FbbzkmY.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Dimensions 3',
        price: '$69',
        image: 'https://i.imgur.com/hOfHRIB.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Inner city blues',
        price: '$69',
        image: 'https://i.imgur.com/jllJqoG.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Kaleidoscope 1',
        price: '$69',
        image: 'https://i.imgur.com/lp79Edu.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Kaleidoscope 2',
        price: '$69',
        image: 'https://i.imgur.com/5Lrs7rA.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Kaleidoscope 3',
        price: '$69',
        image: 'https://i.imgur.com/4xlrXJx.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Kaleidoscope 4',
        price: '$69',
        image: 'https://i.imgur.com/HGd5HXG.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Kaleidoscope 5',
        price: '$69',
        image: 'https://i.imgur.com/gQTPNUp.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Kaleidoscope 6',
        price: '$69',
        image: 'https://i.imgur.com/t5MTmDt.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Kaleidoscope 7',
        price: '$69',
        image: 'https://i.imgur.com/UQKkmj2.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Kaleidoscope 8',
        price: '$69',
        image: 'https://i.imgur.com/4wfBhhy.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'Pieces of Colour',
        price: '$69',
        image: 'https://i.imgur.com/AUsH9zI.jpeg',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consectetur pulvinar massa, vitae faucibus libero tincidunt non. Aliquam erat volutpat. Ut bibendum justo sed rutrum suscipit.',
      },
      {
        title: 'White Lines of Destiny',
        price: '$69',
        image: 'https://i.imgur.com/vSeL90D.jpeg',
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
  margin-bottom: 20px;
  float: left;
  line-height: 0.7;
}

.art-price {
  color: #858585;
  margin-top: 5px;
  padding-top: 7px;
  font-size: 20px;
  margin-bottom: 0px;
}

.art-container {
  height: 100%;
  width: 100%;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
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
