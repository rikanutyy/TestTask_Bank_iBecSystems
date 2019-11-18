<template>
<div>
  <header></header>
  <div>
      <Navbar />
      <nuxt />
  </div>
</div>
</template>

<script>
import Navbar from '@/components/Navbar/Navbar';

export default {
  components: {
    Navbar
  }
}
</script>