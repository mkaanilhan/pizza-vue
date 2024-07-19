<script>
import { RouterLink, RouterView } from 'vue-router'

export default {

  data() {
    return {

      baseUrl: 'https://669a57039ba098ed61ff463c.mockapi.io/api/v1/pizzas'
    }
  }
}
</script>

<template>

  <div class='text-xl'>Welcome</div>

  <RouterView />
</template>
