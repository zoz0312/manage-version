<template>
	<v-app>
    <HelloWorld/>
    <PostCard/>
	</v-app>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import PostCard from '@/components/PostCard.vue'

export default {
  name: 'home',
	data: () => ({
	}),
  components: {
    HelloWorld,
		PostCard,
  }
}
</script>
