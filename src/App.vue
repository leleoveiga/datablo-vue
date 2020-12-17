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
html {
	--scrollbarBG: #1f1f1f;
	--thumbBG: #4a4a4a;
}

body::-webkit-scrollbar {
	width: 16px;
}

body::-webkit-scrollbar-track {
	background: #1c1f23;
}

body::-webkit-scrollbar-thumb {
	background-color: var(--thumbBG);
	border-radius: 0px;
	border: 0px solid var(--scrollbarBG);
}

body::-webkit-scrollbar-thumb:hover {
	background: #575757;
}
</style>
