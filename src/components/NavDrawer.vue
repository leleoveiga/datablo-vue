<template>
	<v-navigation-drawer permanent app clipped right dark>
		<v-list nav>
			<v-list-item v-for="item in items" :key="item.title" link>
				<v-list-item-content class="pa-3">
					<h3 class="font-weight-medium d-flex align-self-center">
						{{ item.title }}
					</h3>
				</v-list-item-content>
			</v-list-item>
		</v-list>
	</v-navigation-drawer>
</template>

<script>
export default {
	name: "NavDrawer",
	data: () => ({
		items: [
			{ title: "Overview", icon: "mdi-view-dashboard" },
			{ title: "Perfil do aluno", icon: "mdi-image" },
			{ title: "Sobre RAE", icon: "mdi-help-box" },
		],
		right: null,
	}),
};
</script>

<style></style>
