<template>
	<v-card class="mt-10" width="90%" dark>
		<div
			class="font-weight-bold body-1 d-flex align-center justify-center mt-10"
		>
			No geral, em comparação com o regime presencial, você acha que o volume de
			atividades exigidas no RAE é:
		</div>

		<div class="d-flex align-center justify-center mt-10">
			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGrafico = 0"
				>Geral</v-btn
			>
			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGrafico = 1"
				>Por Curso</v-btn
			>
			<v-btn class="mx-3" color="#eead2dcc" light @click="tipoGrafico = 2"
				>Por Campus</v-btn
			>
		</div>

		<VolumeAtividadesGeral v-if="tipoGrafico === 0" height="400" />
		<VolumeAtividadesPorCurso v-else-if="tipoGrafico === 1" height="650" />
		<VolumeAtividadesPorCampus v-else-if="tipoGrafico === 2" height="650" />
	</v-card>
</template>

<script>
import VolumeAtividadesGeral from "../../charts/sobreProfessores/volumeAtividades/VolumeAtividadesGeral";
import VolumeAtividadesPorCurso from "../../charts/sobreProfessores/volumeAtividades/VolumeAtividadesPorCurso";
import VolumeAtividadesPorCampus from "../../charts/sobreProfessores/volumeAtividades/VolumeAtividadesPorCampus";

export default {
	name: "VolumeAtividades",
	components: {
		VolumeAtividadesGeral,
		VolumeAtividadesPorCurso,
		VolumeAtividadesPorCampus,
	},
	data: function() {
		return {
			tipoGrafico: 0,
		};
	},
};
</script>

<style></style>
