<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Na sua opinião, em comparação com o regime presencial, no RAE os
			professores estão:
		</div>

		<div class="d-flex align-center justify-center mt-10">
			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGrafico = 0"
				>Geral</v-btn
			>
			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGrafico = 1"
				>Por Curso</v-btn
			>
			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGrafico = 2"
				>Por Campus</v-btn
			>
		</div>

		<ExigenciaProfessoresGeral v-if="tipoGrafico === 0" height="300" />
		<ExigenciaProfessoresPorCurso v-else-if="tipoGrafico === 1" height="650" />
		<ExigenciaProfessoresPorCampus v-else-if="tipoGrafico === 2" height="650" />
	</v-card>
</template>

<script>
import ExigenciaProfessoresGeral from "../../charts/sobreProfessores/exigenciaProfessores/ExigenciaProfessoresGeral";
import ExigenciaProfessoresPorCurso from "../../charts/sobreProfessores/exigenciaProfessores/ExigenciaProfessoresPorCurso";
import ExigenciaProfessoresPorCampus from "../../charts/sobreProfessores/exigenciaProfessores/ExigenciaProfessoresPorCampus";

export default {
	name: "ExigenciaProfessores",
	components: {
		ExigenciaProfessoresGeral,
		ExigenciaProfessoresPorCurso,
		ExigenciaProfessoresPorCampus,
	},
	data: function() {
		return {
			tipoGrafico: 0,
		};
	},
};
</script>

<style></style>
