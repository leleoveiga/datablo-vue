<template>
	<v-app>
		<v-main>
			<Header />
			<NavDrawer />
			<Content />
		</v-main>
	</v-app>
</template>

<script>
import NavDrawer from "./components/NavDrawer";
import Header from "./components/Header";
import Content from "./components/Content";

export default {
	name: "App",

	components: {
		NavDrawer,
		Header,
		Content,
	},
};
</script>
