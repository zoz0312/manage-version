<template>
	<v-card
		height="100%"
		width="256">
			<v-list>
				<div v-for='item in propsdata' :key='item.title'>
					<Item 
						v-if='item.items === undefined || item.items.length === 0'
						v-bind:propsdata='item'/>
					<v-list-group v-else>
						<template v-slot:activator>
							<v-list-item-content>
								<v-list-item-title v-text='item.title'/>
							</v-list-item-content>
						</template>
						<div v-for='item2 in item.items' :key='item2.title'>
							<Item
								v-if='item2.items === undefined || item2.items.length === 0'
								:key='item2.title'
								v-bind:propsdata='item2'/>
							<v-list-group
								v-else
								sub-group
								no-action>
								<template v-slot:activator>
									<v-list-item-content>
										<v-list-item-title v-text='item2.title'/>
									</v-list-item-content>
								</template>
							<Item
								v-for='item3 in item2.items'
								:key='item3.title'
								v-bind:propsdata='item3'/>
							</v-list-group>
						</div>
					</v-list-group>
				</div>
			</v-list>
	</v-card>
</template>

<script>
import Item from '@/components/category/Item.vue'

export default {
	props: ['propsdata'],
  name: 'Navigation',

  data: () => ({
  }),
	components: {
		Item,
	}
};
</script>
<style scope>
.depth2-item {

}
</style>
