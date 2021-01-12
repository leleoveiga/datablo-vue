<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Você acredita que o RAE afetou sua saúde mental para:
		</div>
		<div class="d-flex align-center justify-center mt-10">
			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGraficoSaude = 0"
				>Geral</v-btn
			>

			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGraficoSaude = 1"
				>Por Curso</v-btn
			>
		</div>
		<SaudeMentalGeral
			v-if="tipoGraficoSaude === 0"
			class=""
			height="300"
			width="900"
		/>
		<SaudeMentalPorCurso
			v-else-if="tipoGraficoSaude === 1"
			class=""
			height="500"
			width="900"
		/>
	</v-card>
</template>

<script>
import SaudeMentalGeral from "../../charts/opiniaoRae/saudeMental/SaudeMentalGeral";
import SaudeMentalPorCurso from "../../charts/opiniaoRae/saudeMental/SaudeMentalPorCurso";
export default {
	name: "SaudeMental",
	components: {
		SaudeMentalGeral,
		SaudeMentalPorCurso,
	},
	data: function() {
		return {
			tipoGraficoSaude: 0,
		};
	},
};
</script>

<style></style>
