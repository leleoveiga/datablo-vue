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
						label: "Campina Grande",
						hidden: false,
						data: [51, 202, 230, 56, 26, 10],
						backgroundColor: "#eead2d",
						barThickness: "flex",
					},

					{
						label: "Cajazeiras",
						hidden: true,
						data: [15, 111, 79, 18, 8, 7],
						backgroundColor: "#00F042",
						barThickness: "flex",
					},

					{
						label: "Cuité",
						hidden: true,
						data: [40, 160, 129, 36, 9, 3],
						backgroundColor: "#753bff",
						barThickness: "flex",
					},

					{
						label: "Patos",
						hidden: true,
						data: [1, 11, 25, 15, 7, 2],
						backgroundColor: "#0017F0",
						barThickness: "flex",
					},

					{
						label: "Pombal",
						hidden: true,
						data: [6, 49, 67, 28, 10, 1],
						backgroundColor: "#F00106",
						barThickness: "flex",
					},

					{
						label: "Sousa",
						hidden: true,
						data: [2, 22, 66, 36, 20, 3],
						backgroundColor: "#cf13cb",
						barThickness: "flex",
					},
				],
			},
			{
				maintainAspectRatio: false,
				align: "center",
				layout: {
					padding: 60,
				},

				legend: {
					display: true,
					labels: {
						fontSize: 13,
						fontColor: "#e6e7ea",
						fontFamily: "Roboto",
						boxWidth: 15,
					},
				},

				title: {
					display: false,
					padding: 20,
					text: "por Campi",
					fontSize: 25,
					fontColor: "#e6e7ea",
					fontFamily: "Roboto",
				},

				scales: {
					yAxes: [
						{
							barPercentage: 0.9,

							gridLines: {
								display: false,
							},

							ticks: {
								beginAtZero: true,
								fontSize: 14,
								fontColor: "#e6e7ea",
								fontFamily: "Roboto",
							},

							barThickness: "flex",
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
