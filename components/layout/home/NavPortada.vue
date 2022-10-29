<template>
	<div class="cContainer cContainer--header cContainer--shadow">
		<div class="cContainer cContainer--normal cContainer--flex-colum">
			<div class="cContainer cContainer--top-header cNav">
				<div class="cNav__brand"><img src="@/assets/img/logo-icon.png" />Irmantto MyPyMe</div>
				<div class="cNav__actions">
					<ul class="cNav__list_links">
						<li class="cNav__links">
							<a class="cNav__link">
								<div class="cContainerNavIcon"><i class="fa fa-building"></i></div>
								<div class="cContainerNavText">
									<h6 class="cContainerNavText__h6">Institución Ubicación</h6>
									<p class="cContainerNavText__p">Carretra Central Oesta</p>
								</div>
							</a>
						</li>
						<li class="cNav__links">
							<NuxtLink to="/dashboard" class="cNav__link">
								<div class="cContainerNavIcon"><i class="fas fa-mobile-alt"></i></div>
								<div class="cContainerNavText">
									<h6 class="cContainerNavText__h6">Númiero de Teléfono</h6>
									<p class="cContainerNavText__p">(+53) 51097630</p>
								</div>
							</NuxtLink>
						</li>
						<li class="cNav__links">
							<a class="cNav__link">
								<div class="cContainerNavIcon"><i class="fas fa-envelope"></i></div>
								<div class="cContainerNavText">
									<h6 class="cContainerNavText__h6">Correo Electrónico</h6>
									<p class="cContainerNavText__p">irmanttonline@gmail.com</p>
								</div>
							</a>
						</li>
					</ul>
				</div>
			</div>
			<div class="cContainer cContainer--bottom-header">
				<div class="cContainer cNav">
					<ul class="cNav__list_links">
						<li class="cNav__links">
							<NuxtLink to="/" class="cNav__link cNav__link--gold">Portada</NuxtLink>
						</li>
						<li class="cNav__links">
							<NuxtLink to="/dashboard" class="cNav__link cNav__link--gold">Informacion de la Empresa</NuxtLink>
						</li>
						<li class="cNav__links">
							<NuxtLink to="/dashboard" class="cNav__link cNav__link--gold">Principales Servicios</NuxtLink>
						</li>
						<li class="cNav__links">
							<NuxtLink to="/dashboard" class="cNav__link cNav__link--gold">Registrarse en el Sistema</NuxtLink>
						</li>
						<li class="cNav__links">
							<NuxtLink to="/autenticarse" class="cNav__link cNav__link--gold">Autenticarse en el Sistema</NuxtLink>
						</li>
					</ul>
					<a href="#" class="btn btn-md mb-0 bg-gradient-dark">Contactar Ahora</a>
				</div>
			</div>
		</div>
	</div>
</template>
<style>
	.cContainer {
		display: flex;
		width: 100%;
		height: 100%;
	}
	.cContainer--absolute {
		position: absolute;
		left: 0;
	}
	.cContainer--header {
		background-color: white;
		z-index: 1;
		height: 200px;
		justify-content: center;
	}
	.cContainer--shadow {
		box-shadow: 0 0.75rem 1.0625rem -0.3125rem rgb(12 26 36 / 9%), 0 0.25rem 0.4375rem -0.1875px rgb(12 26 36 / 4%);
	}
	.cContainer--normal {
		max-width: 1300px;
	}
	.cContainer--flex-colum {
		flex-direction: column;
	}
	.cContainer--flex-row {
		flex-direction: row;
	}
	.cContainer--top-header {
		height: 129px;
		border-bottom: 1px rgba(201, 201, 201, 0.5) solid;
	}
	.cContainer--bottom-header {
		height: 70px;
	}
	.cContainer--justify-end {
		justify-content: end;
	}
	.cNav {
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
	}
	.cNav__brand {
		line-height: 50px;
		height: 100%;
		font-family: Noto Sans, sans-serif;
		font-weight: 700;
		font-size: 25px;
		padding: 30px 20px;
		color: #1e293b;
	}
	.cNav__brand img {
		height: 100%;
		margin-right: 10px;
	}
	.cNav__actions {
		display: flex;
		flex-direction: row;
		justify-content: flex-end;
		align-items: center;
		height: 100%;
		padding: 30px 0px;
		flex-grow: 1;
	}
	.cNav__list_links {
		display: flex;
		text-decoration: none;
		padding: 0;
		margin: 0;
	}
	.cNav__links {
		list-style-type: none;
		text-decoration: none;
		margin-right: 30px;
	}
	.cNav__links:last-child {
		margin-right: 0px;
	}
	.cNav__link {
		display: flex;
		flex-direction: row;
		cursor: pointer;
		color: #3c4f6d;
	}
	.cNav__link:hover .cContainerNavText__h6,
	.cNav__link:hover .cContainerNavText__p,
	.cNav__link:hover .cContainerNavIcon i {
		color: #1e293b;
	}
	.cNav__link:hover .cContainerNavIcon {
		border: 1px #1e293b solid;
	}
	.cNav__link.cNav__link--gold {
		font-size: 18px;
	}
	.cNav__link.cNav__link--gold:hover {
		color: goldenrod;
	}
	.cContainerNavIcon {
		display: flex;
		align-items: center;
		justify-content: center;
		margin-right: 10px;
		background-color: gold;
		border-radius: 25px;
		border: 1px transparent;
		width: 50px;
		height: 50px;
	}
	.cContainerNavIcon i {
		font-size: 25px;
	}
	.cContainerNavText {
		display: flex;
		flex-direction: column;
	}
	.cContainerNavText__h6 {
		color: #3c4f6d;
		font-weight: 700;
		margin: 0;
		padding: 0;
	}
	.cContainerNavText__p {
		color: #3c4f6d;
		margin: 0;
		padding: 0;
	}
	.btn.bg-gradient-dark:hover {
		color: #1e293b !important;
		border-color: #1e293b !important;
		background-image: linear-gradient(310deg, #ffd700 0%, #ffd700 100%) !important;
	}
</style>
<style scoped>
	.router-link-exact-active {
		font-weight: 700;
	}
</style>
