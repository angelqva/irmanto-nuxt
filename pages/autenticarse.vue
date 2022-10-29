<template>
	<NuxtLayout :name="layout">
		<div class="cContent">
			<div class="cContent__left"></div>
			<div class="cContent__right"></div>
		</div>
		<div class="container mt-0">
			<div class="row mt-8 justify-content-end">
				<div class="col-12 col-sm-8 col-md-6">
					<div class="card p-4">
						<div class="card-header pb-0">
							<h2 class="text-center">Ingresar al sistema</h2>
							<p class="text-center fs-5 mb-0">Rellene los siguientes campos</p>
						</div>
						<div class="card-body">
							<div class="mx-md-5 mx-2">
								<form @submit="autenticarse">
									<FormText
										v-model.number="data.nombre.value"
										:label="data.nombre.label"
										:minLength="3"
										:maxLength="20"
										:placeholder="'Entre el usuario'"
										:required="true"
										regExp="^[a-zA-Z]*$"
										reg-exp-feed-back="Solo se aceptan caracteres de a-z A-Z sin espacios"
										v-model:errorBackend="data.nombre.errorBackend"
									/>
									<FormPassword
										v-model="data.password.value"
										v-model:valido="data.password.valido"
										v-model:errorBackend="data.password.errorBackend"
										:label="data.password.label"
										placeholder="Introduzca su contraseña"
										:minLength="7"
										:maxLength="50"
										:required="true"
									/>
									<button type="submit" class="btn btn-dark w-100 mt-3 mb-3">Autenticarse</button>
								</form>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</NuxtLayout>
</template>
<style scoped></style>
<script setup lang="ts">
	import { reactive, onMounted, onUnmounted } from "vue";
	const layout: string = "home";
	const data = reactive({
		nombre: {
			label: "Nombre:",
			value: "",
			errorBackend: "",
			valido: false,
			required: true,
		},
		password: {
			label: "Contraseña:",
			value: "",
			minLength: 7,
			maxLength: 30,
			required: true,
			valido: false,
			errorBackend: "",
		},
	});
	const autenticarse = (event: SubmitEvent) => {
		console.log(event.submitter);
		event.preventDefault();

		if (data.nombre.value !== "Angel") {
			data.nombre.errorBackend = "El nombre debe ser Angel";
		} else {
			data.nombre.value = "";
		}
	};
	onMounted(() => {
		data.nombre.value = "";
		data.password.value = "";
	});
	onUnmounted(() => {
		data.nombre.value = "";
		data.password.value = "";
	});
</script>
<style scoped>
	.cContent__left {
		background-image: url("@/assets/img/loginbg.jpg");
		background-position: bottom right;
	}
</style>
