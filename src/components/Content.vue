<template>
	<v-card
		class="d-flex align-center justify-center"
		color="#2f3337"
		height="100%"
		tile
	>
		<!-- <div class="ma-12">ohusadyusaudsa</div> -->
		<v-card class="marginGraph" width="90%" dark>
			<div
				class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
			>
				Quantidade de Respondentes
			</div>
			<div class="d-flex align-center justify-center mt-10">
				<v-btn class="mx-3" color="#eead2dcc">Geral</v-btn>
				<v-btn class="mx-3" color="#eead2dcc">Por curso</v-btn>
				<v-btn class="mx-3" color="#eead2dcc">Por campus</v-btn>
			</div>
			<Quantidade class="mt-n5" height="1750" width="900" />
			<QuantidadePorCurso class="mt-n5" height="485" width="900" />
			<QuantidadePorCampus class="mt-n5" height="380" width="900" />
		</v-card>
	</v-card>
</template>

<script>
import Quantidade from "./graphs/Quantidade";
import QuantidadePorCurso from "./graphs/QuantidadePorCurso";
import QuantidadePorCampus from "./graphs/QuantidadePorCampus";

export default {
	name: "Content",
	components: {
		Quantidade,
		QuantidadePorCurso,
		QuantidadePorCampus,
	},
};
</script>

<style>
.marginGraph {
	margin: 100px 0px 0px 0px;
}
</style>
