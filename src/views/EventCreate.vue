<template>
	<div>
		<h1>Create an Event, {{ user.name }}</h1>
		<p>This event is created by {{ user.name }}</p>
		<p>Total categories {{ categoriesLength }}</p>
		<p>{{ getEventById(1) }} </p>
	</div>
</template>

<script>
import { mapState } from 'vuex'
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters(['categoriesLength', 'getEventById']),
    ...mapState(['categories', 'user'])
  }
}
</script>
