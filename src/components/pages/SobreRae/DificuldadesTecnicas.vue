<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			No que diz respeito a dificuldades técnicas (queda de internet ou energia,
			indisponibilidade de equipamento etc), você passa por elas:
		</div>

		<DificuldadesTecnicasGeral height="300" width="100" />
	</v-card>
</template>

<script>
import DificuldadesTecnicasGeral from "../../charts/opiniaoRae/DificuldadesTecnicasGeral";

export default {
	name: "DificuldadesTecnicas",
	components: {
		DificuldadesTecnicasGeral,
	},
};
</script>

<style></style>
