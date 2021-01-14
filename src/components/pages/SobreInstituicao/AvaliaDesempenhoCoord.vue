<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Como você avalia o desempenho da coordenação do seu curso no atendimento e
			suporte aos estudantes no RAE?
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

		<AvaliaDesempenhoCoordGeral v-if="tipoGrafico === 0" height="400" />
		<AvaliaDesempenhoCoordPorCurso v-else-if="tipoGrafico === 1" height="650" />
		<AvaliaDesempenhoCoordPorCampus
			v-else-if="tipoGrafico === 2"
			height="650"
		/>
	</v-card>
</template>

<script>
import AvaliaDesempenhoCoordGeral from "../../charts/sobreInstituicao/avaliaDesempenhoCoord/AvaliaDesempenhoCoordGeral";
import AvaliaDesempenhoCoordPorCurso from "../../charts/sobreInstituicao/avaliaDesempenhoCoord/AvaliaDesempenhoCoordPorCurso";
import AvaliaDesempenhoCoordPorCampus from "../../charts/sobreInstituicao/avaliaDesempenhoCoord/AvaliaDesempenhoCoordPorCampus";

export default {
	name: "AvaliaUFCG",
	components: {
		AvaliaDesempenhoCoordGeral,
		AvaliaDesempenhoCoordPorCurso,
		AvaliaDesempenhoCoordPorCampus,
	},
	data: function() {
		return {
			tipoGrafico: 0,
		};
	},
};
</script>

<style></style>
