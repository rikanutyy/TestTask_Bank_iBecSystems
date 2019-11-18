<template>
<div class="container">
  <div class="Users">
    <h2 class="user__title">{{pageTitle + ":"}}</h2>
    <h3 class="user__hint">Полное имя:</h3>

    <ul class="user__block">
      <li class="user__list" v-for="user of users" :key="user.id">
        <a class="user__link" href="#" @click.prevent="openUser(user)">{{user.name}}</a>
      </li>
    </ul>
  </div>
</div>
</template>

<script>
export default {
  async fetch({store}) {
    if (store.getters['users/users'].length === 0) {
      await store.dispatch('users/fetch')
    }
  },
  data: () => ({
    pageTitle: 'Пользователи'
  }),
  computed: {
    users() {
      return this.$store.getters['users/users']
    }
  },
  methods: {
    openUser(user) {
      this.$router.push('/users/' + user.id)
    }
  }
}
</script>

<style lang="scss">
	.container {
		margin-top: 25px;
	}
  .Users {
    .user__title {
      color: $text-color;
      font-size: $user-font-size;
    }
    .user__hint {
      color: $user-hint-color;
      font-size: ($user-font-size/1.4);
      margin-left: 20px;
    }
  }
  .user__block {
    color: $text-color;
    .user__list {
      margin: ($default-indent) auto;
    }
    .user__link {
      display: flex;
      color: $text-color;
      background: $navbar-color;
      border: $user-border;
      color: $text-color;
      padding: $padding-user;
      &:hover {
        color: $hover-text-color;
        background: $hover-color;
        transition: .3s all;
      }
    }
  }
</style>