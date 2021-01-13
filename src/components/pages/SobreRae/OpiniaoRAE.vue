<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="px-10 font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			No geral, você acha o RAE:
		</div>

		<OpiniaoRAEGeral height="400" width="100" />
	</v-card>
</template>

<script>
import OpiniaoRAEGeral from "../../charts/opiniaoRae/OpiniaoRAEGeral";

export default {
	name: "OpiniaoRAE",
	components: {
		OpiniaoRAEGeral,
	},
};
</script>

<style></style>
