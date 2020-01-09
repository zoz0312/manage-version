<template>
  <v-app>
		<v-row>
			<v-col cols='3' class='pt-0'>
				<Navigation v-bind:propsdata='category'/>
			</v-col>
			<v-col cols='9'>
				<router-view/>
			</v-col>	
		</v-row>
  </v-app>
</template>

<script>
import Navigation from '@/components/Navigation.vue'
export default {
  name: 'App',

  data: () => ({
		category: [
			{ title: 'Home', src:'/' },
			{ title: 'APC', items: [
				{ title:'v02.00.00', src:'/apc/2' },
				{ title:'v03.00.00', src:'/apc/3' },
				{ title:'v04.00.00', src:'/apc/4' },
				{ title:'v05.00.00', src:'/apc/5' },
				{ title:'v06.00.00', src:'/apc/6' },
			] },
		],
  }),
	components: {
		Navigation,
	}
};
</script>
<style scope>
</style>
