<template>
	<v-navigation-drawer class="pt-4" permanent app clipped right color="#1c1f23">
		<v-treeview
			v-model="tree"
			:open="initiallyOpen"
			:items="items"
			activatable
			item-key="name"
			open-on-click
		>
			<template v-slot:label="{ item }">
				<h3 class="grey--text text--lighten-4 font-weight-light">
					{{ item.name }}
				</h3>
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
			{ name: "Perfil do aluno" },
			{ name: "Sobre RAE" },
		],
		right: null,
	}),
};
</script>

<style></style>
