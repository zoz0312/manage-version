<template>
	<v-app>
		{{ id }}
	</v-app>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'list',
  components: {
  },
  data: () => ({
    id: 0
  }),
	created() {
		this.id = this.$route.params.id;
	}
}
</script>
