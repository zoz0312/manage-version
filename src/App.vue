<template>
  <v-app>
		<router-link to='/'>MAIN</router-link>
		<router-link to='/about'>About</router-link>
		<router-link to='/list/1'>List 1</router-link>
		<router-view/>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
