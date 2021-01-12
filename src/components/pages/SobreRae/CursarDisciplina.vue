<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Com relação às disciplinas que queria cursar, você conseguiu se matricular
			em:
		</div>

		<CursarDisciplinaGeral height="300" width="100" />
	</v-card>
</template>

<script>
import CursarDisciplinaGeral from "../../charts/opiniaoRae/CursarDisciplinaGeral";

export default {
	name: "CursarDisciplina",
	components: {
		CursarDisciplinaGeral,
	},
};
</script>

<style></style>
