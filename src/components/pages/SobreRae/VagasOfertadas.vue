<template>
	<v-card class="marginGraph" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Você acredita que as vagas ofertadas no RAE foram suficientes?
		</div>
		<div class="d-flex align-center justify-center mt-10">
			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGraficoVagas = 0"
				>Geral</v-btn
			>

			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGraficoVagas = 1"
				>Por Curso</v-btn
			>
		</div>
		<VagasOfertadasGeral
			v-if="tipoGraficoVagas === 0"
			class=""
			height="250"
			width="900"
		/>
		<VagasOfertadasPorCurso
			v-else-if="tipoGraficoVagas === 1"
			class=""
			height="500"
			width="900"
		/>
	</v-card>
</template>

<script>
import VagasOfertadasGeral from "../../charts/opiniaoRae/vagasOfertadas/VagasOfertadasGeral";
import VagasOfertadasPorCurso from "../../charts/opiniaoRae/vagasOfertadas/VagasOfertadasPorCurso";
export default {
	name: "VagasOfertadas",
	components: {
		VagasOfertadasGeral,
		VagasOfertadasPorCurso,
	},
	data: function() {
		return {
			tipoGraficoVagas: 0,
		};
	},
};
</script>

<style></style>
