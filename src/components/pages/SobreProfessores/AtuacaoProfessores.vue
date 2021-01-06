<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Na sua opinião, os professores são tolerantes com imprevistos que
			impossibilitem a realização de atividades?
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

		<AtuacaoProfessoresGeral v-if="tipoGrafico === 0" height="400" />
		<AtuacaoProfessoresPorCurso v-else-if="tipoGrafico === 1" height="650" />
		<AtuacaoProfessoresPorCampus v-else-if="tipoGrafico === 2" height="650" />
	</v-card>
</template>

<script>
import AtuacaoProfessoresGeral from "../../charts/sobreProfessores/atuacaoProfessores/AtuacaoProfessoresGeral";
import AtuacaoProfessoresPorCurso from "../../charts/sobreProfessores/atuacaoProfessores/AtuacaoProfessoresPorCurso";
import AtuacaoProfessoresPorCampus from "../../charts/sobreProfessores/atuacaoProfessores/AtuacaoProfessoresPorCampus";

export default {
	name: "AtuacaoProfessores",
	components: {
		AtuacaoProfessoresGeral,
		AtuacaoProfessoresPorCurso,
		AtuacaoProfessoresPorCampus,
	},
	data: function() {
		return {
			tipoGrafico: 0,
		};
	},
};
</script>

<style></style>
