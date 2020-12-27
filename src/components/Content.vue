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

		<PerfilRespondentes />
		<SobreRae />
	</v-card>
</template>

<script>
import PerfilRespondentes from "./pages/PerfilRespondentes";
import SobreRae from "./pages/SobreRae.vue";

export default {
	name: "Content",
	components: {
		PerfilRespondentes,
		SobreRae,
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
