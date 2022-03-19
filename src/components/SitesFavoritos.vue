<template>
  <div class="sites-favoritos">
    <h2>Sites Favoritos</h2>
    <ul>
      <li v-for="site of sites" :key="site.id">
        <a :href="site.link">{{ site.nome }}</a>
      </li>
    </ul>
    <ul class="agora">
      <li v-for="user of users.result" :key="user.ctrl_user" class="list-users">
        <article>First Name: {{ user.first_name }}</article>
        <article>Last Name: {{ user.last_name }}</article>
        <article>User: {{ user.user }}</article>
        <article>Email: {{ user.email }}</article>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SitesFavoritos",
  data() {
    return {
      sites: [],
      users: [],
    };
  },
  created() {
    fetch("https://hackthon-decola.firebaseio.com/sites-favoritos.json")
      .then((result) => result.json())
      .then((json) => {
        this.sites = json;
      }),
      fetch("http://localhost:8087/api/users", { method: "get" })
        .then((res) => {
          res.json().then((result) => {
            this.users = result;
            console.log(this.users);
          });
        })
        .catch((error) => {
          console.log(error);
        });
  },
};
</script>

<style scoped>
li {
  list-style-type: none;
}
.list-users {
  margin-bottom: 15px;
  padding: 0px;
  width: 300px;
  height: auto;
}
.agora {
  display: flex;
  align-items: center;
  flex-direction: column;
}
</style>