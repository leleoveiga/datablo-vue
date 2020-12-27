<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			No geral, você acha que essas dificuldades prejudicam o seu desempenho?
		</div>

		<DificuldadesDesempenhoGeral height="300" width="100" />
	</v-card>
</template>

<script>
import DificuldadesDesempenhoGeral from "../../charts/opiniaoRae/DificuldadesDesempenhoGeral";

export default {
	name: "DificuldadesDesempenho",
	components: {
		DificuldadesDesempenhoGeral,
	},
};
</script>

<style></style>
