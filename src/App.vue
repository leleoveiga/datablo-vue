<template>
	<v-app>
		<link rel="preconnect" href="https://fonts.gstatic.com" />
		<link
			href="https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@100;200;300;400;500;600;700;800&display=swap"
			rel="stylesheet"
		/>
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
