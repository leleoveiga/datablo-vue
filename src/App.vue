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

<style>
body::-webkit-scrollbar {
	width: 16px;
}

body::-webkit-scrollbar-track {
	background: #1c1f23;
}

body::-webkit-scrollbar-thumb {
	background-color: #4a4a4a;
	border-radius: 0px;
	border: 0px solid #1f1f1f;
}

body::-webkit-scrollbar-thumb:hover {
	background: #575757;
}
</style>
