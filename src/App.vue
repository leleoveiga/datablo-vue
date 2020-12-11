<template>
	<v-app>
		<v-main>
			<Header />
			<NavDrawer />
		</v-main>
	</v-app>
</template>

<script>
import NavDrawer from "./components/NavDrawer";
import Header from "./components/Header";

export default {
	name: "App",

	components: {
		NavDrawer,
		Header,
	},
};
</script>
