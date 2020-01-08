<template>
	<v-app>
    <Navigation v-bind:propsdata='category'/>
    <HelloWorld/>
    <ListItem v-bind:propsdata='item'/>
    <PostCard/>
	</v-app>
</template>

<script>
// @ is an alias to /src
import Navigation from '@/components/Navigation.vue'
import HelloWorld from '@/components/HelloWorld.vue'
import ListItem from '@/components/ListItem.vue'
import PostCard from '@/components/PostCard.vue'

export default {
  name: 'home',
	data: () => ({
		item: {
			id: 0,
			category: 'APC',
			apply_range: 'SC2000',
			version: 'v06.00.02',
			main_desc: '테이블 추가',
			sub_desc: '~~변경 및 ~~수정 완료',
			attach: null,
			attach_name: '18_tbl_insert.sql',
			date: '20/01/06'
		},
		category: [
			{ title: 'Dashboard', items: [
				{ title:'title2222' }
			] },
			{ title: 'Photos', items: [] },
			{ title: 'About', items: [] },
		],
	}),
  components: {
		Navigation,
    HelloWorld,
		ListItem,
		PostCard,
  }
}
</script>
