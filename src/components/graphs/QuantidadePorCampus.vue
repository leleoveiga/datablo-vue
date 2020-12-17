<script>
import { HorizontalBar } from "vue-chartjs";

export default {
	name: "BarChart",
	extends: HorizontalBar,
	mounted() {
		this.renderChart(
			{
				labels: [
					"Campina Grande",
					"Cuité",
					"Cajazeiras",
					"Pombal",
					"Sousa",
					"Patos",
					"Sumé",
				],

				datasets: [
					{
						data: [575, 377, 238, 161, 149, 61, 6],
						backgroundColor: "#EEAD2D",
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
					labels: {
						fontSize: 15,
						fontColor: "white",
						fontFamily: "roboto",
					},
					position: "right",
				},

				title: {
					display: false,
					padding: 30,
					text: "Nº de Respondentes/Campi",
					fontSize: 25,
					fontColor: "#d3d3d3",
					fontFamily: "roboto",
				},

				scales: {
					yAxes: [
						{
							display: true,
							gridLines: {
								display: false,
							},

							barThickness: 23,

							ticks: {
								beginAtZero: true,
								fontSize: 14,
								fontColor: "#e6e7ea",
								fontFamily: "Roboto",
							},
						},
					],

					xAxes: [
						{
							display: false,
							ticks: {
								beginAtZero: true,
								fontSize: 14,
								fontColor: "#e6e7ea",
								fontFamily: "Roboto",
							},

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
