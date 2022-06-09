<template>
  <div class="home">
    <div class="title-insta">
      <h1>GramInsta</h1>

    </div>
    <div class="container-post">
      <CardPost :post="post" @like="post.like ++" v-for="post in posts" :key='post.title'/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import CardPost from "@/components/CardPost.vue";

export default {
  name: 'HomeView',
  components: {
    CardPost,
  },
  data(){
    return {
      posts: [
        {
          img: 'https://picsum.photos/200',
          title: 'Post 1',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          like: 0,
        },
        {
          img: 'https://picsum.photos/200',
          title: 'Post 2',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          like: 0,
        },
        {
          img: 'https://picsum.photos/200',
          title: 'Post 3',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          like: 0,
        },
        {
          img: 'https://picsum.photos/200',
          title: 'Post 4',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          like: 0,
        },
      ]
    }
}
}
</script>

<style lang="scss">
.title-insta{
  background: rgb(64,93,230);
  background: linear-gradient(180deg, rgba(64,93,230,1) 0%, rgba(88,81,219,1) 11%, rgba(131,58,180,1) 22%, rgba(193,53,132,1) 33%, rgba(225,48,108,1) 44%, rgba(253,29,29,1) 55%, rgba(245,96,64,1) 66%, rgba(247,119,55,1) 77%, rgba(252,175,69,1) 88%, rgba(255,220,128,1) 99%);
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;

  h1{
    font-size: 100px;
    margin: 0;
  }
}
.container-post {
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap;
  width: 100%;
  height: 100%;
}
</style>
