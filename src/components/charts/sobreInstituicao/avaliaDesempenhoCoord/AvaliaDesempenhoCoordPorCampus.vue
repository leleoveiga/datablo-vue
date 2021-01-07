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
					"Bom",
					"Regular",
					"Ruim",
					"Péssimo",
					"Não Responderam",
				],
				datasets: [
					{
						label: "Campina Grande",
						hidden: false,
						data: [162, 204, 98, 42, 32, 37],
						backgroundColor: "#EEAD2D",
						barThickness: "flex",
					},

					{
						label: "Cajazeiras",
						hidden: true,
						data: [55, 92, 59, 11, 9, 12],
						backgroundColor: "#00F042",
						barThickness: "flex",
					},

					{
						label: "Cuité",
						hidden: true,
						data: [61, 148, 103, 24, 19, 22],
						backgroundColor: "#753bff",
						barThickness: "flex",
					},

					{
						label: "Patos",
						hidden: true,
						data: [5, 19, 22, 9, 4, 2],
						backgroundColor: "#0017F0",
						barThickness: "flex",
					},

					{
						label: "Pombal",
						hidden: true,
						data: [59, 49, 40, 3, 7, 3],
						backgroundColor: "#F00106",
						barThickness: "flex",
					},

					{
						label: "Sousa",
						hidden: true,
						data: [12, 33, 43, 27, 17, 17],
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
