<template>
	<v-list-item :to='propsdata.src'>
		<v-list-item-content>
			<v-list-item-title v-text='propsdata.title'/>
		</v-list-item-content>
	</v-list-item>
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
.depth2-item {

}
</style>
