<script>
import { HorizontalBar } from "vue-chartjs";

export default {
	name: "BarChart",
	extends: HorizontalBar,
	mounted() {
		this.renderChart(
			{
				labels: [
					"Direito",
					"Eng Civil",
					"Ciência da Computação",
					"Eng Elétrica",
					"Geografia",
					"Ciências Biológicas",
					"Nutrição",
					"Farmácia",
					"Enfermagem",
					"Matemática",
					"História",
					"Medicina",
					"Design",
					"Química",
					"Administração",
					"Eng de Petróleo",
					"Arte e Mídia",
					"Letras",
					"Estatística",
					"Eng Ambiental",
					"Psicologia",
					"Eng de Alimentos",
					"Eng Mecânica",
					"Física",
					"Filosofia",
					"Eng Florestal",
					"Eng Agrícola",
					"Eng Química",
					"Eng de Produção",
					"Pedagogia",
					"Ciências Sociais",
					"Arquitetura e Urbanismo",
					"Agronomia",
					"Odontologia",
					"Meteorologia",
					"Medicina Veterinária",
					"Ciências Econômicas",
					"Eng de Minas",
					"Eng de Materiais",
					["Eng de Biotecnologia", "e Bioprocessos."],
					"Ciências Contábeis",
					"Gestão Pública",
					"Eng de Biossistemas",
					"Comunicação Social",
				],
				datasets: [
					{
						label: "Quantidade",
						data: [
							138,
							128,
							114,
							112,
							99,
							92,
							90,
							82,
							73,
							71,
							66,
							63,
							53,
							46,
							38,
							37,
							34,
							25,
							25,
							25,
							24,
							24,
							12,
							10,
							9,
							8,
							8,
							7,
							7,
							6,
							5,
							5,
							5,
							4,
							4,
							4,
							3,
							2,
							2,
							2,
							2,
							1,
							1,
							1,
						],
						backgroundColor: "#EEAD2D",
					},
				],
			},
			{
				maintainAspectRatio: false,
				layout: {
					padding: 60,
				},

				legend: {
					display: false,
					/*                         labels: {
                            fontSize: 15,
                            fontColor: "#e6e7ea",
                            fontFamily: 'Roboto',
                        },
*/
				},

				title: {
					display: false,
					padding: 20,
					text: "Nº de Respondentes",
					fontSize: 25,
					fontColor: "#e6e7ea",
					fontFamily: "Roboto",
				},

				scales: {
					yAxes: [
						{
							barPercentage: 1,

							gridLines: {
								display: false,
							},

							ticks: {
								beginAtZero: true,
								fontSize: 14,
								fontColor: "#e6e7ea",
								fontFamily: "Roboto",
							},

							barThickness: 23,
						},
					],

					xAxes: [
						{
							display: false,
							gridLines: {
								display: false,
							},
						},
					],
				},
			}
		);
	},
};
</script>

<style></style>
