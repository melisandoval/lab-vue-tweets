<template>
  <div className="actions">
    <!-- Font Awesome icons -->
    <i class="far fa-comment"></i>
    <i class="fas fa-retweet"></i>
    <i v-if="!likedTweet" class="far fa-heart heart" @click="like"></i>
    <span v-else @click="like">❤️</span>
    <i class="fas fa-share"></i>
  </div>
</template>

<script>
export default {
  data: () => ({
    likedTweet: false,
  }),
  methods: {
    like() {
      this.likedTweet = !this.likedTweet;
    },
  },
};
</script>

<style scoped></style>
