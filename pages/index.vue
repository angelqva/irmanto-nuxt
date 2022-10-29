<template>
	<NuxtLayout :name="layout">
		<div class="cContent">
			<div class="cContent__left"></div>
			<div class="cContent__right"></div>
		</div>
		<div class="container mt-0">
			<div class="cContainer cContainer--justify-end">
				<div class="cBoxInfo">
					<div class="cBoxInfo__card shadow-lg">
						<h2 class="cBoxInfo__h2">Estamos Dedicados a la Excelencia en la Reparación y Mantenimiento.</h2>
						<p class="cBoxInfo__p">
							Contamos con exelentes trabajadores dedicados a resolver lo antes posible los problemas de nuestros clientes. Estamos atentos a sus solicitudes 24/7.
						</p>
						<div class="cBoxActions">
							<a href="#" class="btn btn-lg mb-0 bg-gradient-gold">Autenticarse</a>
							<a href="#" class="btn btn-lg mb-0 bg-gradient-dark">Tienes Cuenta? Registrate Ahora</a>
						</div>
					</div>
				</div>
			</div>
		</div>
	</NuxtLayout>
</template>
<script lang="ts" setup>
	const layout: string = "home";
</script>
<style>
	.cContent {
		position: absolute;
		top: 200px;
		left: 0px;
		width: 100%;
		display: flex;
		flex-direction: row;
		z-index: -5;
	}
	.cContent__left {
		width: 65%;
		background-image: url("@/assets/img/split/installing-an-air-conditioner-in-an-apartment-offi-2021-12-09-22-09-41-utc-min.jpg");
		background-size: cover;
		height: 719px;
	}
	.cContent__right {
		background-color: #0b1b69;
		width: 35%;
		height: 719px;
	}
	.cBoxInfo {
		display: flex;
		align-items: center;
		justify-content: center;
		height: 719px;
		width: 800px;
	}
	.cBoxInfo__card {
		background-color: white;
		width: 700px;
		height: 463px;
		border-radius: 4px;
		padding: 40px;
	}
	.cBoxInfo__h2 {
		font-size: 46px;
	}
	.cBoxInfo__p {
		font-size: 22px;
	}
	.cBoxActions {
		display: flex;
		flex-direction: row;
		margin-top: 40px;
		justify-content: space-around;
	}
	.btn.bg-gradient-gold {
		color: #1e293b;
		border-color: #1e293b;
		background-image: linear-gradient(310deg, #ffd700 0%, #ffd700 100%);
	}
	.btn.bg-gradient-gold:hover {
		color: #ffffff;
		border-color: transparent;
		background-image: linear-gradient(310deg, #1e293b 0%, #1e293b 100%);
	}
</style>
