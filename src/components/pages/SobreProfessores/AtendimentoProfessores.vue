<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Na sua experiência, o atendimento individual dos professores aos alunos
			está sendo:
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

		<AtendimentoProfessoresGeral v-if="tipoGrafico === 0" height="370" />
		<AtendimentoProfessoresPorCurso
			v-else-if="tipoGrafico === 1"
			height="650"
		/>
		<AtendimentoProfessoresPorCampus
			v-else-if="tipoGrafico === 2"
			height="650"
		/>
	</v-card>
</template>

<script>
import AtendimentoProfessoresGeral from "../../charts/sobreProfessores/atendimentoProfessores/AtendimentoProfessoresGeral";
import AtendimentoProfessoresPorCurso from "../../charts/sobreProfessores/atendimentoProfessores/AtendimentoProfessoresPorCurso";
import AtendimentoProfessoresPorCampus from "../../charts/sobreProfessores/atendimentoProfessores/AtendimentoProfessoresPorCampus";

export default {
	name: "AtendimentoProfessores",
	components: {
		AtendimentoProfessoresGeral,
		AtendimentoProfessoresPorCurso,
		AtendimentoProfessoresPorCampus,
	},
	data: function() {
		return {
			tipoGrafico: 0,
		};
	},
};
</script>

<style></style>
