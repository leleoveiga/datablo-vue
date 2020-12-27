<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Na sua opinião, a qualidade do ensino no RAE, em comparação com o
			presencial, é:
		</div>

		<QualidadeRAEGeral height="300" width="100" />
	</v-card>
</template>

<script>
import QualidadeRAEGeral from "../../charts/opiniaoRae/QualidadeRAEGeral";

export default {
	name: "QualidadeRAE",
	components: {
		QualidadeRAEGeral,
	},
};
</script>

<style></style>
