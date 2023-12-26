<template>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {

    }
  },
  mounted() {
    this.fun()
  },
  methods: {
    fun() {
      axios.get('https://api.giphy.com/v1/gifs/trending?api_key=O0WPlsebm26FrZQELgaSjvxRcP5cbQvf')
          .then((response) => {
            console.log(response.data); // Выводим данные в консоль
          })
          .catch((error) => {
            console.error('Ошибка', error)
          })
    },
  },
}
</script>
