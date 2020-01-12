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
				{ title:'v02.00.00', items: [
					{ title: 'v02.00.00', src:'/list/apc/1/1' },
					{ title: 'v02.00.02', src:'/list/apc/1/2' },
					{ title: 'v02.00.04', src:'/list/apc/1/3' },
				]},
				{ title:'v03.00.00', items: [
					{ title: 'v03.00.02', src:'/list/apc/2/1' },
					{ title: 'v03.00.04', src:'/list/apc/2/2' },
				]},
				{ title:'v04.00.00', items:[
					{ title: 'v04.00.02', src:'/list/apc/3/1' },
					{ title: 'v04.00.04', src:'/list/apc/3/2' },
				]},
				{ title:'v05.00.00', items:[
					{ title: 'v05.00.02', src:'/list/apc/4/1' },
					{ title: 'v05.00.04', src:'/list/apc/4/2' },
				]},
				{ title:'v06.00.00', items:[
					{ title: 'v06.00.02', src:'/list/apc/5/1' },
					{ title: 'v06.00.04', src:'/list/apc/5/2' },
				]},
			]},
		],
  }),
	components: {
		Navigation,
	}
};
</script>
<style scope>
</style>
