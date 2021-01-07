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
		<v-treeview
			v-model="tree"
			:items="items"
			item-key="name"
			activatable
			color="#eead2d"
			expand-icon=""
			transition
			open-on-click
		>
			<template v-slot:label="{ item }">
				<span
					v-bind:class="{ childrenFont: item.child }"
					class="navFont grey--text text--lighten-4 font-weight-regular"
					@click="scrollTo(item.id)"
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
			{ name: "Sobre RAE", id: "sobreRae" },
		],
		right: null,
	}),
	methods: {
		scrollTo(id) {
			this.$vuetify.goTo(`#${id}`, {
				duration: 200,
				offset: 0,
				easing: "easeInOutCubic",
			});
		},
	},
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
