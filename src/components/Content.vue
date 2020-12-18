<template>
	<v-card
		class="d-flex flex-column align-center mt-10"
		color="#2f3337"
		height="100%"
		tile
	>
		<!-- Template dos textos
		<strong class="mt-16" style="font-size: 2em"></strong>
		<div class="textGraphs">
			<p class="p1 grey--text text--lighten-4"></p>
		</div>
		-->
		<div style="width: 90%">
			<p class="titlePage grey--text text--lighten-4">
				Resultados da consulta de opinião pública da comunidade acadêmica de
				graduação da UFCG a respeito do Regime Acadêmico Extraordinário - RAE
			</p>
			<!-- <div class="d-flex justify-start"> -->
			<v-btn class="px-10 mb-16" color="#eead2dcc">Metodologia</v-btn>
			<div class="presentation">
				<div class="text">
					<p class=" grey--text text--lighten-4">
						Ao longo do Regime Acadêmico Extraordinário (RAE) da UFCG, ouvimos
						diversas queixas e comentários de alunos sobre os mais variados
						aspectos, desde a falta de vagas até a baixa qualidade do ensino em
						algumas disciplinas. Apesar de serem pertinentes, nos demos conta de
						que, naturalmente, as opiniões que nos atingem são, frequentemente,
						reflexos da "bolha" social em que nos encontramos. Nasceu aí o
						questionamento, será que os estudantes de outros campi ou de outros
						cursos passam por essas mesmas situações? Será a nossa realidade
						compartilhada pelos outros graduandos?
					</p>
					<p class=" grey--text text--lighten-4">
						Para conseguir essas respostas, nós fizemos o que qualquer bom
						estudante faz diariamente: Perguntar. Assim começou a nossa jornada,
						cheia de pedras pelo caminho, e o resultado é o que vocês
						encontrarão a seguir. Infelizmente, ao longo do desenvolvimento,
						encontramos diversos pontos fracos que certamente serão reforçados
						em atividades futuras. Não há problema algum em cometer erros, desde
						que eles sejam usados como degraus para o progresso, certo?
					</p>
					<p class=" grey--text text--lighten-4">
						Também gostaríamos de dizer que esta pesquisa de opinião foi
						desenvolvida por estudantes e para estudantes, com o objetivo de dar
						voz à comunidade acadêmica de graduação, que raramente tem seus
						anseios e opiniões ouvidos. Por isso, esperamos que esta seja a
						primeira de muitas e que vocês encontrem aqui um ambiente de
						representatividade.
					</p>
					<p class=" grey--text text--lighten-4">
						Por fim, deixamos registrado o agradecimento à Assessoria de
						Comunicação da UFCG, que nos ajudou a divulgar o projeto, elevando o
						número de respondentes a níveis aceitáveis. Agradecemos também aos
						CAs e às diversas coordenações, que repassaram nosso formulário aos
						estudantes, e aos prórios alunos, que tiveram a boa vontade de
						opinar. Sem vocês nada teria sido possível.
					</p>
				</div>
			</div>
		</div>
		<!-- </div> -->
		<!-- <v-btn>Github</v-btn> -->

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
	</v-card>
</template>

<script>
import QuantidadeGeral from "./graphs/quantidade/QuantidadeGeral";
import QuantidadePorCurso from "./graphs/quantidade/QuantidadePorCurso";
import QuantidadePorCampus from "./graphs/quantidade/QuantidadePorCampus";
import VagasOfertadasGeral from "./graphs/vagasOfertadas/VagasOfertadasGeral";
import VagasOfertadasPorCurso from "./graphs/vagasOfertadas/VagasOfertadasPorCurso";

export default {
	name: "Content",
	components: {
		QuantidadeGeral,
		QuantidadePorCurso,
		QuantidadePorCampus,
		VagasOfertadasGeral,
		VagasOfertadasPorCurso,
	},
	data: function() {
		return {
			tipoGraficoQuantidade: 0,
			tipoGraficoVagas: 0,
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
	margin-top: 50px;
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
