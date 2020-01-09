<template>
	<v-card
		height="100%"
		width="256">
			<v-list>
				<div v-for='item in propsdata' :key='item.title'>
					<v-list-item
						v-if='item.items === undefined || item.items.length === 0'
						:to='item.src'>
						<v-list-item-content>
							<v-list-item-title v-text='item.title'/>
						</v-list-item-content>
					</v-list-item>
					<v-list-group v-else>
						<template v-slot:activator>
							<v-list-item-content>
								<v-list-item-title v-text='item.title'/>
							</v-list-item-content>
						</template>
						<v-list-item
							v-for='item2 in item.items'
							:key='item2.title'
							:to='item2.src'>
							<v-list-item-content>
								<v-list-item-title class='ml-3' v-text='item2.title'/>
							</v-list-item-content>
						</v-list-item>
					</v-list-group>
				</div>
			</v-list>
	</v-card>
</template>

<script>
export default {
	props: ['propsdata'],
  name: 'Navigation',

  data: () => ({
  }),
};
</script>
<style scope>
.depth2-item {

}
</style>
