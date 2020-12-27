<template>
	<div class="d-flex flex-column align-center mt-1">
		<strong class="mt-16" style="font-size: 2em"
			>Perfil dos Respondentes</strong
		>
		<div class="textGraphs">
			<p class="p1 grey--text text--lighten-4">
				Ao todo, 1567 estudantes, o que corresponde a pouco menos de 10% do
				total de alunos de graduação da UFCG, responderam à pesquisa de opinião
				ao longo de duas semanas, dos quais a maior parte são dos campi de
				Campina Grande, Cuité e Cajazeiras, que juntos representam mais de 75%
				dos respondentes.
			</p>
			<p class="p1 grey--text text--lighten-4">
				Além disso, é notável que a grande maioria dos participantes se
				encontram nos períodos iniciais de seus cursos. Cerca de 43% deles ainda
				não chegaram no 4º período letivo. Percebe-se, com isso, que o
				engajamento nesta consulta tende a ser consideravelmente menor entre os
				estudantes mais veteranos.
			</p>
		</div>
		<!-- card dos gráficos -->
		<v-card class="marginGraph" width="90%" dark>
			<div
				class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
			>
				Quantidade de Respondentes
			</div>
			<div class="d-flex align-center justify-center mt-10">
				<v-btn
					class="mx-3"
					color="#eead2dcc"
					light
					@click="tipoGraficoQuantidade = 0"
					>Geral</v-btn
				>
				<v-btn
					class="mx-3"
					color="#eead2dcc"
					light
					@click="tipoGraficoQuantidade = 1"
					>Por curso</v-btn
				>
				<v-btn
					class="mx-3"
					color="#eead2dcc"
					light
					@click="tipoGraficoQuantidade = 2"
					>Por campus</v-btn
				>
			</div>
			<!-- <v-expand-transition> -->
			<QuantidadeGeral
				v-if="tipoGraficoQuantidade === 0"
				class="mt-n5"
				height="1750"
				width="900"
			/>
			<QuantidadePorCurso
				v-else-if="tipoGraficoQuantidade === 1"
				class="mt-n5"
				height="485"
				width="900"
			/>
			<QuantidadePorCampus
				v-else-if="tipoGraficoQuantidade === 2"
				class="mt-n5"
				height="380"
				width="900"
			/>
			<!-- </v-expand-transition> -->
		</v-card>
	</div>
</template>

<script>
import QuantidadeGeral from "../graphs/quantidade/QuantidadeGeral";
import QuantidadePorCurso from "../graphs/quantidade/QuantidadePorCurso";
import QuantidadePorCampus from "../graphs/quantidade/QuantidadePorCampus";

export default {
	name: "PerfilRespondentes",
	components: {
		QuantidadeGeral,
		QuantidadePorCurso,
		QuantidadePorCampus,
	},
	data: function() {
		return {
			tipoGraficoQuantidade: 0,
		};
	},
};
</script>

<style></style>
