<template>
	<v-card
		class="d-flex flex-column align-center mt-10"
		color="#2f3337"
		height="100%"
		tile
	>
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
			<Quantidade
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

		<div class="textGraphs">
			<p class="p1 grey--text text--lighten-4"></p>
		</div>
	</v-card>
</template>

<script>
import Quantidade from "./graphs/Quantidade";
import QuantidadePorCurso from "./graphs/QuantidadePorCurso";
import QuantidadePorCampus from "./graphs/QuantidadePorCampus";

export default {
	name: "Content",
	components: {
		Quantidade,
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

<style>
.marginGraph {
	margin: 100px 0px 0px 0px;
}
.titlePage {
	margin-top: 200px;
	font-size: 27px;
	max-width: 500px;
	text-align: start;
	margin-block-end: 1em;
}
.presentation {
	/* padding: 60px; */
	margin-top: 150px;
	max-height: 520px;
	/* justify-content: center; */
	-webkit-column-count: 2;
	column-count: 2;
	grid-column-gap: 20px;
	-webkit-column-gap: 20px;
	column-gap: 20px;
	font-size: 1.2rem;
	line-height: 26px;
	/* width: 90%; */
	margin-right: 20%;
	margin-bottom: 50px;
}

.textGraphs {
	margin-top: 40px;
	width: 85%;
	max-height: 520px;
	-webkit-column-count: 2;
	column-count: 2;
	grid-column-gap: 20px;
	-webkit-column-gap: 20px;
	column-gap: 20px;
	font-size: 1.2rem;
	line-height: 26px;
}
strong {
	color: #eead2d;
}
</style>
