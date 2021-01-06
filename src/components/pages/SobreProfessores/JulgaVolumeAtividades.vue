<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			Você julga esse volume de atividades abusivo?
		</div>

		<JulgaVolumeAtividadesGeral height="250" width="100" />
	</v-card>
</template>

<script>
import JulgaVolumeAtividadesGeral from "../../charts/sobreProfessores/JulgaVolumeAtividadesGeral";

export default {
	name: "JulgaVolumeAtividades",
	components: {
		JulgaVolumeAtividadesGeral,
	},
};
</script>

<style></style>
