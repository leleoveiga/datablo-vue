<template>
	<v-card
		class="d-flex flex-column align-center mt-10"
		color="#2f3337"
		height="100%"
		tile
	>
		<!-- Template dos textos
		<div class="d-flex flex-column align-center mt-1">
			<strong class="mt-16" style="font-size: 2em"></strong>

			<div class="textGraphs">
				<p class="p1 grey--text text--lighten-4"></p>
			</div>
		</div>

		Gráficos

		<v-card class="mt-10" width="90%" dark>
			<div
				class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
			>
				Texto do gráfico
			</div>

			<div class="d-flex align-center justify-center mt-10">
				<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGrafico = 0">Botoes</v-btn>
				<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGrafico = 1">Botoes</v-btn>
			</div>

			<Charts/>

		</v-card>
		-->
		<div
			class="grey--text text--lighten-4"
			style="width: 90%; margin-top: 200px;"
		>
			<h1
				class="ml-n2"
				style="font-size: 2.5rem; text-shadow: 2px 2px 3px #000;"
			>
				<v-icon color="#eead2d" size="72">mdi-database</v-icon> Consulta RAE
			</h1>
			<p class="titlePage">
				Resultados da consulta de opinião pública da comunidade acadêmica de
				graduação da UFCG a respeito do Regime Acadêmico Extraordinário - RAE
			</p>
			<!-- <div class="d-flex justify-start"> -->
			<!-- <v-btn
				class="px-10 mb-16"
				color="#eead2dcc"
				>Metodologia</v-btn
			> -->

			<div class="textGraphs" id="overview">
				<p class="p1 grey--text text--lighten-4">
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
				<p class="p1 grey--text text--lighten-4">
					Para conseguir essas respostas, nós fizemos o que qualquer bom
					estudante faz diariamente:<strong> Perguntar</strong>. Assim começou a
					nossa jornada, cheia de pedras pelo caminho, e o resultado é o que
					vocês encontrarão a seguir. Infelizmente, ao longo do desenvolvimento,
					encontramos diversos pontos fracos que certamente serão reforçados em
					atividades futuras. Não há problema algum em cometer erros, desde que
					eles sejam usados como degraus para o progresso, certo?
				</p>
				<p class="p1 grey--text text--lighten-4">
					Também gostaríamos de dizer que esta pesquisa de opinião foi
					desenvolvida por estudantes e para estudantes, com o objetivo de dar
					voz à comunidade acadêmica de graduação, que raramente tem seus
					anseios e opiniões ouvidos. Por isso, esperamos que esta seja a
					primeira de muitas e que vocês encontrem aqui um ambiente de
					representatividade.
				</p>
				<p class="p1 grey--text text--lighten-4">
					Por fim, deixamos registrado o agradecimento à
					<strong>Assessoria de Comunicação</strong> da UFCG, que nos ajudou a
					divulgar o projeto, elevando o número de respondentes a níveis
					aceitáveis. Agradecemos também aos CAs e às diversas coordenações, que
					repassaram nosso formulário aos estudantes, e aos prórios alunos, que
					tiveram a boa vontade de opinar. Sem vocês nada teria sido possível.
				</p>
			</div>
		</div>

		<PerfilRespondentes id="perfilRespondente" />

		<SobreRae id="sobreRae" />
		<VagasOfertadas id="vagasOfertadas" />
		<CursarDisciplina id="cursarDisciplina" />
		<OpiniaoRAE id="opiniaoRae" />
		<DesempenhoRAE id="desempenhoRae" />
		<QualidadeRAE id="qualidadeRae" />
		<SaudeMental id="saudeMentalRae" />
		<DificuldadesTecnicas id="dificuldadesTecnicas" />
		<DificuldadesDesempenho id="dificuldadesDesempenho" />

		<SobreProfessores id="sobreProfessores" />
		<ToleranciaProfessores id="toleranciaProfessores" />
		<AtuacaoProfessores id="atuacaoProfessores" />
		<AtendimentoProfessores id="atendimentoProfessores" />
		<ExigenciaProfessores id="exigenciaProfessores" />
		<VolumeAtividades id="volumeAtividades" />
		<JulgaVolumeAtividades id="julgaVolumeAtividades" />

		<SobreInstituicao id="sobreInstituicao" />
		<AvaliaUFCGPandemia id="avaliaUFCGPandemia" />
		<AvaliaDesempenhoCoord id="avaliaDesempenhoCoord" />
		<Metodologia id="metodologia" />
	</v-card>
</template>

<script>
import PerfilRespondentes from "./pages/PerfilRespondentes";
import VagasOfertadas from "./pages/SobreRae/VagasOfertadas.vue";
import SobreRae from "./pages/SobreRae/SobreRae.vue";
import CursarDisciplina from "./pages/SobreRae/CursarDisciplina.vue";
import OpiniaoRAE from "./pages/SobreRae/OpiniaoRAE.vue";
import DesempenhoRAE from "./pages/SobreRae/DesempenhoRAE.vue";
import QualidadeRAE from "./pages/SobreRae/QualidadeRAE.vue";
import SaudeMental from "./pages/SobreRae/SaudeMental.vue";
import DificuldadesDesempenho from "./pages/SobreRae/DificuldadesDesempenho.vue";
import DificuldadesTecnicas from "./pages/SobreRae/DificuldadesTecnicas.vue";
import SobreProfessores from "./pages/SobreProfessores/SobreProfessores";
import ToleranciaProfessores from "./pages/SobreProfessores/ProfessoresTolerantes";
import AtuacaoProfessores from "./pages/SobreProfessores/AtuacaoProfessores";
import ExigenciaProfessores from "./pages/SobreProfessores/ExigenciaProfessores";
import AtendimentoProfessores from "./pages/SobreProfessores/AtendimentoProfessores";
import VolumeAtividades from "./pages/SobreProfessores/VolumeAtividades";
import JulgaVolumeAtividades from "./pages/SobreProfessores/JulgaVolumeAtividades";
import SobreInstituicao from "./pages/SobreInstituicao/SobreInstituicao";
import AvaliaUFCGPandemia from "./pages/SobreInstituicao/AvaliaUFCGPandemia";
import AvaliaDesempenhoCoord from "./pages/SobreInstituicao/AvaliaDesempenhoCoord";
import Metodologia from "./pages/Metodologia&Informacoes";

export default {
	name: "Content",
	components: {
		Metodologia,
		AvaliaDesempenhoCoord,
		AvaliaUFCGPandemia,
		SobreInstituicao,
		JulgaVolumeAtividades,
		VolumeAtividades,
		AtendimentoProfessores,
		ExigenciaProfessores,
		AtuacaoProfessores,
		ToleranciaProfessores,
		SobreProfessores,
		DificuldadesTecnicas,
		DificuldadesDesempenho,
		SaudeMental,
		QualidadeRAE,
		DesempenhoRAE,
		OpiniaoRAE,
		CursarDisciplina,
		SobreRae,
		PerfilRespondentes,
		VagasOfertadas,
	},
	data: function() {
		return {};
	},
};
</script>

<style>
.marginGraph {
	margin: 100px 0px 0px 0px;
}
.titlePage {
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
	box-sizing: border-box;
	margin-top: 50px;
	width: 85%;
	/* max-height: 520px; */
	/* -webkit-column-count: 2; */
	column-count: 2;
	grid-column-gap: 20px;
	-webkit-column-gap: 20px;
	column-gap: 20px;
	font-size: 1.2rem;
	line-height: 26px;
}

.avaliacao_cursos {
	color: #e6e7ea !important;
	font-size: 0.9rem;
	font-family: "Roboto", sans-serif;
	color: var(--text-color);
	line-height: 23px;
	column-count: 2;
}

strong {
	color: #eead2d !important;
}

.outLink {
	text-decoration: none;
	color: #77db48 !important;
}
</style>
