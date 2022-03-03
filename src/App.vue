<template>
  <section class="container">
    <h2>{{ user.name }}</h2>
    <h2>{{ user.age }}</h2>
    <button @click="version">change the version</button>
  </section>
</template>

<script>
import { reactive } from 'vue';

export default {
  setup() {
    //1----you can take only one const and add you data in to it with below method and ref is use for all kind of data types and objects
    //where react is only use for object
    // const user = ref('Bhumik');
    // const uAge = ref(21);

    //2---you can make one object for user and define your value liek below
    const user = reactive({
      name: 'Vue with option api',
      age: 1,
    });

    function changeAge() {
      user.age = 2;
    }

    return { user: user, version: changeAge };
  },

  // data() {
  //   return {
  //     userName: 'Bhumik kalola',
  //   };
  // },
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}

.container {
  margin: 3rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
  text-align: center;
}
</style>
