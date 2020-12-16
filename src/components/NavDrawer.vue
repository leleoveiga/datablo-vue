<template>
	<v-navigation-drawer
		class="pt-8"
		permanent
		app
		clipped
		right
		color="#1c1f23"
		width="375px"
	>
		<link rel="preconnect" href="https://fonts.gstatic.com" />
		<link
			href="https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@100;200;300;400;500;600;700;800&display=swap"
			rel="stylesheet"
		/>
		<v-treeview
			v-model="tree"
			:items="items"
			item-key="name"
			transition
			open-on-click
		>
			<template v-slot:label="{ item }">
				<span
					v-bind:class="{ childrenFont: item.child }"
					class="navFont grey--text text--lighten-4 font-weight-regular"
				>
					{{ item.name }}
				</span>
			</template>
		</v-treeview>
	</v-navigation-drawer>
</template>

<script>
export default {
	name: "NavDrawer",
	data: () => ({
		items: [
			{ name: "Overview" },
			{
				name: "Perfil do aluno",
				children: [
					{
						name: "Quantidade de respostas",
						child: true,
					},
				],
			},
			{ name: "Sobre RAE" },
		],
		right: null,
	}),
};
</script>

<style>
.navFont {
	font-family: "Roboto Slab", serif;
	font-size: 22px;
}
.childrenFont {
	font-family: "Roboto Slab", serif;
	font-size: 16px;
}
</style>
