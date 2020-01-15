<template>
	<v-app>
    <PostCard/>
		<button @click='test'>asads</button>
		P Category {{ p_category }}
	</v-app>
</template>

<script>
import PostCard from '@/components/PostCard.vue'

export default {
  name: 'Form',
  data: () => ({
		p_category: null
  }),
	created() {
	},
	methods: {
		test(){
		}
	},
	components: {
		PostCard,
	}
}
</script>
