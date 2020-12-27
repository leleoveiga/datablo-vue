<template>
	<div class="d-flex flex-column align-center mt-1">
		<strong class="mt-16" style="font-size: 2em">Sobre o RAE</strong>

		<div class="textGraphs">
			<p class="p1 grey--text text--lighten-4">
				Depois de questionados sobre diversos aspectos do RAE (Regime Acadêmico
				Extraordinário), fica aparente a baixa popularidade do mesmo entre os
				estudantes de graduação. Quando perguntada diretamente, por exemplo, sua
				opinião geral sobre o sistema, 41% o classificaram como ruim ou péssimo
				em contraste aos 21% que declararam opinião positiva.
			</p>
			<p class="p1 grey--text text--lighten-4">
				Em questões mais específicas, a impopularidade do regime fica ainda mais
				evidente: 71% dos respondentes avaliam a qualidade do ensino como pior,
				em relação ao presencial. Além disso, 91% dos consultados declararam ter
				tido, ao menos uma vez, algum tipo de problema técnico que dificultou ou
				inviabilizou a realização de atividades nesse período. Destes, 79% dizem
				ter seu desempenho afetado por esses imprevistos.
			</p>
		</div>

		<v-card class="marginGraph" width="90%" dark>
			<div
				class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
			>
				Você acredita que as vagas ofertadas no RAE foram suficientes?
			</div>
			<div class="d-flex align-center justify-center mt-10">
				<v-btn
					class="mx-3"
					color="#eead2dcc"
					light
					@click="tipoGraficoVagas = 0"
					>Geral</v-btn
				>

				<v-btn
					class="mx-3"
					color="#eead2dcc"
					light
					@click="tipoGraficoVagas = 1"
					>Por Curso</v-btn
				>
			</div>
			<VagasOfertadasGeral
				v-if="tipoGraficoVagas === 0"
				class=""
				height="230"
				width="900"
			/>
			<VagasOfertadasPorCurso
				v-else-if="tipoGraficoVagas === 1"
				class=""
				height="500"
				width="900"
			/>
		</v-card>
	</div>
</template>

<script>
import VagasOfertadasGeral from "../graphs/vagasOfertadas/VagasOfertadasGeral";
import VagasOfertadasPorCurso from "../graphs/vagasOfertadas/VagasOfertadasPorCurso";
export default {
	name: "SobreRae",
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
