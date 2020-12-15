<template>
	<v-app-bar
		clipped-right
		app
		color="primary"
		dark
		scroll-off-screen
		scroll-threshold="50"
	>
		<v-icon color="#eead2d" size="36">mdi-database</v-icon>
		<div class="d-flex align-center">
			<p class="ma-0 display-1">Datablo</p>
		</div>

		<v-spacer></v-spacer>

		<v-btn href="https://github.com/leleoveiga" target="_blank" text>
			<span class="mr-2">github</span>
			<v-icon>mdi-open-in-new</v-icon>
		</v-btn>
	</v-app-bar>
</template>

<script>
export default {
	name: "Header",
};
</script>

<style></style>
