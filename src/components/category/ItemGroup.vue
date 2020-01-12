<template>
	<v-list-group>
		<template v-slot:activator>
			<v-list-item-content>
				<v-list-item-title v-text='item.title'/>
			</v-list-item-content>
		</template>
		<Item
		v-for='item2 in item.items'
		:key='item2.title'
		v-bind:propsdata='item2'/>
	</v-list-group>
</template>
<script>
export default {
	props: ['propsdata'],
  name: 'Item',

  data: () => ({
  }),
};
</script>
<style scope>
</style>
