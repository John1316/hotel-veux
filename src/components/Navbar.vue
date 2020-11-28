<template>
	<!--start Navbar -->
	<nav class="navbar navbar-expand-lg navbar-light bg-dark navbar-stick-dark" data-navbar="sticky">
		<div class="container-fluid">
			<div class="navbar-left">
				<a class="navbar-brand" href="#">
					<img src="img/logo/logo1.png" alt="" class="logo-90px">
					<router-link class="navbar-brand text-white" to="/">NKN</router-link>
				</a>
			</div>
			<div class="navbar-right">
				<button class="navbar-toggler" type="button">&#9776;</button>
			</div>

			<section class="navbar-mobile">
				<nav class="nav nav-navbar m-auto">
					<router-link class="nav-link active" to="/">Home</router-link>
					<a class="nav-link" href="#">Hotels</a>
					<li class="nav-item">
						<a class="nav-link" href="#">Promotions <span class="arrow"></span></a>
						<nav class="nav">
							<router-link class="nav-link fs-18 text-dark" to="/promotions">1st class</router-link>
							<router-link class="nav-link fs-18 text-dark" to="/promotions">2nd class</router-link>
							<router-link class="nav-link fs-18 text-dark" to="/promotions">3rd class</router-link>
						</nav>
					</li>
					<a class="nav-link" href="#">Destinations</a>
					<a class="nav-link" href="#">Vouchers</a>
					<router-link class="nav-link" to="">About us</router-link>
				</nav>

				<div>
					<router-link class="text-white ml-lg-4 mr-2" to="/signup" id="login">Sign Up</router-link>
					<router-link class="btn border-main rounded text-main ml-lg-4 mr-2" to="/signup" id="login">Sign in</router-link>
				</div>
			</section>
		</div>
	</nav>
	<!-- end navbar -->
</template>
			