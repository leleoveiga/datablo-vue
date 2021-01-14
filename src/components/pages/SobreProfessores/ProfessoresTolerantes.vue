<template>
	<v-card class="marginGraph" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Na sua opinião, os professores são tolerantes com imprevistos que
			impossibilitem a realização de atividades?
		</div>

		<div class="d-flex flex-wrap align-center justify-center mt-10">
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

		<ProfessoresTolerantesGeral v-if="tipoGrafico === 0" height="250" />
		<ProfessoresTolerantesPorCurso v-else-if="tipoGrafico === 1" />
		<ProfessoresTolerantesPorCampus v-else-if="tipoGrafico === 2" />
	</v-card>
</template>

<script>
import ProfessoresTolerantesGeral from "../../charts/sobreProfessores/toleranciaProfessores/ProfessoresTolerantesGeral";
import ProfessoresTolerantesPorCurso from "../../charts/sobreProfessores/toleranciaProfessores/ProfessoresTolerantesPorCurso";
import ProfessoresTolerantesPorCampus from "../../charts/sobreProfessores/toleranciaProfessores/ProfessoresTolerantesPorCampus";

export default {
	name: "ProfessoresTolerantes",
	components: {
		ProfessoresTolerantesGeral,
		ProfessoresTolerantesPorCurso,
		ProfessoresTolerantesPorCampus,
	},
	data: function() {
		return {
			tipoGrafico: 0,
		};
	},
};
</script>

<style></style>
