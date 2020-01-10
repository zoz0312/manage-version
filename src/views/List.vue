<template>
	<v-app>
		{{ id }}

    <ListItem v-bind:propsdata='item'/>
	</v-app>
</template>

<script>
import ListItem from '@/components/ListItem.vue'

export default {
  name: 'list',
  data: () => ({
    id: 0,
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
  }),
	created() {
		this.updateId();
	},
	watch: {
		'$route':'updateId'
	},
	methods: {
		updateId () {
			this.id = this.$route.params.id;
		}
	},
	components: {
		ListItem,
	}
}
</script>
