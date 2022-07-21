<template>
  <section>
    <friend-nav />
    <friend-form />
    <section class="main">
    <h2>All Friends</h2>
    <friend-card v-for="user of allusers" :key="user" :user="user" />
    </section>
  </section>
</template>

<script>
import FriendNav from './components/FriendNav.vue'
import FriendForm from './components/FriendForm.vue'
import FriendCard from './components/FriendCard.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    FriendNav,
    FriendForm,
    FriendCard
  },
  data() {
    return {
      allusers: [],
    }
  },
  mounted() {
    axios.get('http://127.0.0.1:81/api/people').then(res => {
      this.allusers = res.data;
    })
  }
}
</script>

<style>
  * {
    margin: 0;
  }
  .main {
    margin-top: 20px;
    }
  h2 {
    text-align: center;

  }

</style>









