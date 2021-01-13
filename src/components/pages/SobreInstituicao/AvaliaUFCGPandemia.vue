<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Como você avalia a atuação da UFCG diante da pandemia?
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

		<AvaliaUFCGPandamiaGeral v-if="tipoGrafico === 0" height="400" />
		<AvaliaUFCGPandamiaPorCurso v-else-if="tipoGrafico === 1" height="650" />
		<AvaliaUFCGPandamiaPorCampus v-else-if="tipoGrafico === 2" height="650" />
	</v-card>
</template>

<script>
import AvaliaUFCGPandamiaGeral from "../../charts/sobreInstituicao/avaliaUFCGPandemia/AvaliaUFCGPandemiaGeral";
import AvaliaUFCGPandamiaPorCurso from "../../charts/sobreInstituicao/avaliaUFCGPandemia/AvaliaUFCGPandemiaPorCurso";
import AvaliaUFCGPandamiaPorCampus from "../../charts/sobreInstituicao/avaliaUFCGPandemia/AvaliaUFCGPandemiaPorCampus";

export default {
	name: "AvaliaUFCG",
	components: {
		AvaliaUFCGPandamiaGeral,
		AvaliaUFCGPandamiaPorCurso,
		AvaliaUFCGPandamiaPorCampus,
	},
	data: function() {
		return {
			tipoGrafico: 0,
		};
	},
};
</script>

<style></style>
