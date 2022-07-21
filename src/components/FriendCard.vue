<template>
    <section>
        <h3>{{fullname}}</h3>
        <p>{{user.comment}}</p>
    </section>
</template>

<script>
export default {
  props: {
    user: Object,
  },
  computed: {
    fullname() {
        return this.user.firstname + ' ' + this.user.lastname;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    section {
        width: 40%;
        margin: auto;
        padding: 20px;
        border-radius: 10px;
        margin-top: 15px;
        box-shadow: 0 2px 8px rgba(34, 32, 32, 0.26);
        background: rgb(214, 210, 210);
        border-top: 4px solid rgb(189, 46, 46);
    }
    p {
        margin-top: 10px;
    }
</style>
