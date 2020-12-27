<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Você acredita que o seu desempenho no RAE, em comparação com o presencial:
		</div>

		<DesempenhoRAEGeral height="300" width="100" />
	</v-card>
</template>

<script>
import DesempenhoRAEGeral from "../../charts/opiniaoRae/DesempenhoRAEGeral";

export default {
	name: "DesempenhoRAE",
	components: {
		DesempenhoRAEGeral,
	},
};
</script>

<style></style>
