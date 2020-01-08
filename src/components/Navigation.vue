<template>
	<v-card
		height="400"
		width="256"
		class="mx-auto">
			<v-list>
				<div v-for='item in propsdata' :key='item.title'>
					<v-list-item
						v-if='item.items.length === 0'
						@click='item'>
						{{ item.title }}
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
							@click='item2'>
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
