<template>
	<v-app>
		<v-app-bar clipped-right app color="primary" dark>
			<div class="d-flex align-center">
				<p class="ma-0 display-1">Datablo</p>
			</div>

			<v-spacer></v-spacer>

			<v-btn href="https://github.com/leleoveiga" target="_blank" text>
				<span class="mr-2">github</span>
				<v-icon>mdi-open-in-new</v-icon>
			</v-btn>
		</v-app-bar>

		<v-main>
			<NavDrawer />
		</v-main>
	</v-app>
</template>

<script>
import NavDrawer from "./components/NavDrawer";

export default {
	name: "App",

	components: {
		NavDrawer,
	},
};
</script>
