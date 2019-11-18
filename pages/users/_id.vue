<template>
  <div class="container">
    <h1>{{user.name}}</h1>

    <hr>

    <h3>Почта: {{user.email}}</h3>
    <h3>Телефон: {{user.phone}}</h3>
  </div>
  <!-- Сделаю потом (◕‿◕) -->
</template>

<script>
export default {
  validate({params}) {
    return /^\d+$/.test(params.id)
  },
  async asyncData({$axios, params}) {
    const user = await $axios.$get('https://jsonplaceholder.typicode.com/users/' + params.id)
    return {user}
  }
}
</script>

<style lang="scss" scoped>
	.container {
		margin-top: 25px;
	}
</style>