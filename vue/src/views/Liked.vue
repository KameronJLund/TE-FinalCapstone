<template>
  <main id="liked-page">
    <side-bar id="side-bar-home" />
    <header class="page-title">
      <h1 class="page-title-text">Your Liked Posts</h1>

      <img class="page-title-icon" src="@/assets/icons8-heart-24.png" alt="" />
    </header>
    <image-column class="image-column" />
  </main>
</template>

<script>
import SideBar from "../components/SideBar.vue";
import ImageColumn from "../components/ImageColumn.vue";
import LikeService from '../services/LikeService';

export default {
  components: { ImageColumn, SideBar },
  name: "liked",
  created() {
    LikeService.getLikedPosts().then((response) => {
      this.$store.commit("INITIALIZE_POSTS", response.data);
    });
  },
};
</script>

<style>
main > .page-title {
  /* width: calc(100% - 315px); */
  margin-left: 295px;
  margin-right: auto;
  /* padding-top: 20px; */
  padding-top: 0px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
main > .page-title > .page-title-text {
  color: beige;
}

main > .page-title > .page-title-icon {
  background: beige;
  -webkit-background-clip: border-box;
  margin-left: 10px;
  border-radius: 4px;
  height: 32px;
}
</style>