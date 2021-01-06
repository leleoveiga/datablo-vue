<script>
import { HorizontalBar } from "vue-chartjs";

export default {
	name: "BarChart",
	extends: HorizontalBar,
	mounted() {
		this.renderChart(
			{
				labels: [
					"Excelente",
					"Boa",
					"Razoável",
					"Ruim",
					"Péssima",
					"Não Responderam",
				],

				datasets: [
					{
						data: [115, 557, 598, 191, 80, 26],
						backgroundColor: "#EEAD2D",
						barThickness: "flex",
						hoverBackgroundColor: "#b8831c",
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
					text: "Atuação dos professores é:",
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
