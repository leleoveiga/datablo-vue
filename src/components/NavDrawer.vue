<template>
	<v-navigation-drawer
		class="pt-8"
		permanent
		app
		clipped
		right
		color="#1c1f23"
		width="375px"
	>
		<v-treeview
			:items="items"
			activatable
			color="#eead2d"
			expand-icon=""
			transition
			open-on-click
		>
			<template v-slot:label="{ item }">
				<div
					v-bind:class="{ childrenFont: item.child }"
					class="navFont grey--text text--lighten-4 font-weight-regular"
					style="padding: 11px 0px"
					@click="scrollTo(item.id, item.offs)"
				>
					{{ item.name }}
				</div>
			</template>
		</v-treeview>
	</v-navigation-drawer>
</template>

<script>
export default {
	name: "NavDrawer",
	data: () => ({
		items: [
			{ name: "Overview", id: "overview", offs: 100 },
			{
				name: "Perfil do aluno",
				id: "perfilRespondente",
				children: [
					{
						name: "Quantidade de respostas",
						id: "quantidadeRespostas",
						child: true,
						offs: 40,
					},
				],
			},
			{
				name: "Sobre RAE",
				id: "sobreRae",
				children: [
					{
						name: "Vagas Ofertadas",
						id: "vagasOfertadas",
						child: true,
						offs: 40,
					},
					{
						name: "Disciplinas Cursadas",
						id: "cursarDisciplina",
						child: true,
						offs: 40,
					},
					{
						name: "Opinião Geral",
						id: "opiniaoRae",
						child: true,
						offs: 40,
					},
					{
						name: "Desempenho no RAE",
						id: "desempenhoRae",
						child: true,
						offs: 40,
					},
					{
						name: "Qualidade do Ensino",
						id: "qualidadeRae",
						child: true,
						offs: 40,
					},
					{
						name: "Saúde Mental",
						id: "saudeMentalRae",
						child: true,
						offs: 40,
					},
					{
						name: "Dificuldades Técnicas",
						id: "dificuldadesTecnicas",
						child: true,
						offs: 40,
					},
					{
						name: "Impacto das Dificuldades",
						id: "dificuldadesDesempenho",
						child: true,
						offs: 40,
					},
				],
			},
			{
				name: "Sobre Professores",
				id: "sobreProfessores",
				children: [
					{
						name: "Tolerância dos Professores",
						id: "toleranciaProfessores",
						child: true,
						offs: 40,
					},
					{
						name: "Atuação dos Professores",
						id: "atuacaoProfessores",
						child: true,
						offs: 40,
					},
					{
						name: "Atendimento Individual",
						id: "atendimentoProfessores",
						child: true,
						offs: 40,
					},
					{
						name: "Exigência dos Professores",
						id: "exigenciaProfessores",
						child: true,
						offs: 40,
					},
					{
						name: "Volume de Atividades no RAE",
						id: "volumeAtividades",
						child: true,
						offs: 40,
					},
					{
						name: "Sobre essas Atividades",
						id: "julgaVolumeAtividades",
						child: true,
						offs: 40,
					},
				],
			},
			{
				name: "Sobre Instituição",
				id: "sobreInstituicao",
				children: [
					{
						name: "Avaliação da UFCG",
						id: "avaliaUFCGPandemia",
						child: true,
						offs: 40,
					},
					{
						name: "Desempenho das Coordenações",
						id: "avaliaDesempenhoCoord",
						child: true,
						offs: 40,
					},
				],
			},
			{
				name: "Metodologia",
				id: "metodologia",
				offs: 40,
			},
		],
		right: null,
	}),
	methods: {
		scrollTo(id, offs) {
			// console.log("click");
			this.$vuetify.goTo(`#${id}`, {
				duration: 500,
				offset: offs ? offs : 0,
				easing: "easeOutCubic",
			});
			// var elmnt = document.getElementById(id);
			// elmnt.scrollIntoView({ behavior: "smooth" });
		},
	},
};
</script>

<style>
.navFont {
	font-family: "Roboto Slab", serif;
	font-size: 22px;
}
.childrenFont {
	font-family: "Roboto Slab", serif;
	font-size: 16px;
}
</style>
