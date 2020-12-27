<script>
import { HorizontalBar } from "vue-chartjs";

export default {
	name: "BarChart",
	extends: HorizontalBar,
	mounted() {
		this.renderChart(
			{
				labels: ["Todas", "Algumas", "Nenhuma", "Não Responderam"],

				datasets: [
					{
						data: [708, 788, 48, 23],
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
					text: "você conseguiu se matricular em:",
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
