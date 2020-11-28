<template>
	<!-- start header Section  -->
	<div class="homeView">
		<!-- start header Section  -->
		<header class="header">
			<div class="container">
				<div class="row align-items-end h-100">
					<div
						class="col-md-12 justify-content-center align-items-center text-center text-white"
					>
						<form action="">
							<div class="form-group input-group p-2 bg-white my-5">
								<div class="col-lg-3 col-12 px-1">
									<div class="input-group">
										<div class="input-group-prepend">
											<span class="input-group-text"
												><i class="fa fa-map-marker"></i
											></span>
										</div>
										<input
											type="text"
											class="form-control mr-3"
											placeholder="Destinations"
										/>
									</div>
								</div>
								<div class="col-lg-3 col-12 px-1">
									<div class="input-group">
										<div class="input-group-prepend">
											<span class="input-group-text"
												><i class="fa fa-calendar-alt"></i
											></span>
										</div>
										<input
											type="text"
											class="form-control mr-3"
											placeholder="Check in - Check out"
										/>
									</div>
								</div>
								<div class="col-lg-4 col-12 px-1">
									<div class="input-group">
										<div class="input-group-prepend">
											<span class="input-group-text"
												><i class="fa fa-user"></i
											></span>
										</div>
										<input
											type="text"
											class="form-control mr-3"
											placeholder="0 Aldults - 0 Child - 0 Room"
										/>
									</div>
								</div>

								<div class="col-lg-2 col-12 p-0">
									<router-link to="/searchdetails"
										class="btn btn-lg text-main btn-dark"
										type="button"
									>
										<i
											class="fas fa-search mr-2"
											aria-hidden="true"
										></i
										>Search
									</router-link>
								</div>
							</div>
						</form>
					</div>
				</div>
			</div>
		</header>
		<!-- end header section -->

		<!-- start Promotions -->
		<section class="promotions py-5">
			<div class="container">
				<div class="row no-gutters justify-content-between">
					<h1>Best promotions</h1>
					<nav>
						<div class="nav nav-tabs" id="nav-tab" role="tablist">
							<a
								class="nav-link active"
								id="nav-home-tab"
								data-toggle="tab"
								href="#combo"
								role="tab"
								aria-controls="nav-home"
								aria-selected="true"
								>Combo</a
							>
							<a
								class="nav-link"
								id="nav-profile-tab"
								data-toggle="tab"
								href="#hotels"
								role="tab"
								aria-controls="nav-profile"
								aria-selected="false"
								>Hotels</a
							>
						</div>
					</nav>
					<h5>View all</h5>
				</div>
				<div class="row py-4">
					<div class="col-12 col-md-6 col-lg-4" v-for="item in list" v-bind:key="item.id">
						<div class="promotions__card card d-block">
							<a class="text-decoration-none" href="/promotions">
								<img class="card-img-top" v-bind:src='item.image' alt="Card image cap"/>
								<div class="right">
                                    <div class="ribbon d-flex justify-content-center align-items-center">
                                        <span class="fs-20 text-main ranking">{{item.discount}}%</span>
                                    </div>
                                </div>
								<div class="card-body px-0">
									<h4 class="font-weight-bold">
										{{item.title}}
									</h4>
									<div class="row no-gutters">
										<i class="fas fa-hotel mb-0 mr-2 pt-2"></i>
										<p class="mb-0 mr-2">JW Mariot</p>
										<ul class="list-unstyled d-flex mb-0 mr-2">
											<li>
												<i
													class="fas fa-star text-main mr-1"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas fa-star text-main mr-1"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas fa-star text-main mr-1"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas fa-star text-main mr-1"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas fa-star text-main mr-1"
													aria-hidden="true"
												></i>
											</li>
										</ul>
									</div>
								</div>
							</a>
						</div>
					</div>
				</div>
			</div>
		</section>
		<!-- end Promotions -->

		<!-- start section destination -->
		<section class="destination py-6">
			<div class="container">
				<div class="row no-gutters justify-content-between">
					<h1 class="font-weight-bold">Destination</h1>
					<nav>
						<div class="nav nav-tabs" id="nav-tab" role="tablist">
							<a
								class="nav-link active"
								id="nav-home-tab"
								data-toggle="tab"
								href="#combo"
								role="tab"
								aria-controls="nav-home"
								aria-selected="true"
								>Vietnam</a
							>
							<a
								class="nav-link"
								id="nav-profile-tab"
								data-toggle="tab"
								href="#hotels"
								role="tab"
								aria-controls="nav-profile"
								aria-selected="false"
								>Myanmar</a
							>
							<a
								class="nav-link"
								id="nav-home-tab"
								data-toggle="tab"
								href="#combo"
								role="tab"
								aria-controls="nav-home"
								aria-selected="true"
								>Thailand</a
							>
							<a
								class="nav-link"
								id="nav-profile-tab"
								data-toggle="tab"
								href="#hotels"
								role="tab"
								aria-controls="nav-profile"
								aria-selected="false"
								>Philippines</a
							>
						</div>
					</nav>
					<h5>View all</h5>
				</div>

				<Slick class="slider-arrows-circle-light" v-bind="settings" :options="slickOptions2" :arrows="true" >
					<div class="p-2">
						<div class="destination__card card d-block">
							<img
								class="card-img-top"
								src="img/destination1.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1 text-center">
								<p class="mb-0">Hoi An</p>
							</div>
						</div>
					</div>
					<div class="p-2">
						<div class="destination__card card d-block">
							<img
								class="card-img-top"
								src="img/destination2.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1 text-center">
								<p class="mb-0">Nha Trang</p>
							</div>
						</div>
					</div>
					<div class="p-2">
						<div class="destination__card card d-block">
							<img
								class="card-img-top"
								src="img/destination3.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1 text-center">
								<p class="mb-0">Cat Ba</p>
							</div>
						</div>
					</div>
					<div class="p-2">
						<div class="destination__card card d-block">
							<img
								class="card-img-top"
								src="img/destination4.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1 text-center">
								<p class="mb-0">Da Nang</p>
							</div>
						</div>
					</div>
					<div class="p-2">
						<div class="destination__card card d-block">
							<img
								class="card-img-top"
								src="img/destination5.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1 text-center">
								<p class="mb-0">Phu Quoc</p>
							</div>
						</div>
					</div>
					<div class="p-2">
						<div class="destination__card card d-block">
							<img
								class="card-img-top"
								src="img/destination5.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1 text-center">
								<p class="mb-0">Hoi An</p>
							</div>
						</div>
					</div>
					<div class="p-2">
						<div class="destination__card card d-block">
							<img
								class="card-img-top"
								src="img/destination6.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1 text-center">
								<p class="mb-0">Da Nang</p>
							</div>
						</div>
					</div>
					<div class="p-2">
						<div class="destination__card card d-block">
							<img
								class="card-img-top"
								src="img/destination7.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1 text-center">
								<p class="mb-0">Da Nang</p>
							</div>
						</div>
					</div>
				</Slick>
			</div>
		</section>
		<!-- end section destination -->

		<!-- start section recomends -->
		<section class="recomends py-6">
			<div class="container">
				<div class="row no-gutters justify-content-between">
					<h2 class="font-weight-bold">Recomends for you</h2>
					<nav>
						<div class="nav nav-tabs" id="nav-tab" role="tablist">
							<a
								class="nav-link active"
								id="nav-home-tab"
								data-toggle="tab"
								href="#combo"
								role="tab"
								aria-controls="nav-home"
								aria-selected="true"
								>Hotels/Resorts</a
							>
							<a
								class="nav-link"
								id="nav-profile-tab"
								data-toggle="tab"
								href="#hotels"
								role="tab"
								aria-controls="nav-profile"
								aria-selected="false"
								>Combo</a
							>
							<a
								class="nav-link"
								id="nav-home-tab"
								data-toggle="tab"
								href="#combo"
								role="tab"
								aria-controls="nav-home"
								aria-selected="true"
								>Voucher</a
							>
							<a
								class="nav-link"
								id="nav-profile-tab"
								data-toggle="tab"
								href="#hotels"
								role="tab"
								aria-controls="nav-profile"
								aria-selected="false"
								>Philippines</a
							>
						</div>
					</nav>
					<h5>View all</h5>
				</div>
				<div class="recomends__row no row py-6">
					<div class="col-lg-6 col-12 mb-5">
						<div class="card">
							<div class="row  align-items-center">
								<div class="col-lg-5 col-12 p-0">
									<img
										class="card-img-top"
										src="img/safari1.jpg"
										alt=""
									/>
								</div>
								<div class="col-lg-7 col-12">
									<div class="card-body p-0">
										<h3 class="font-weight-bold">
											Family Safari Vacation To The Home Of The Gods
										</h3>
										<ul class="list-unstyled d-flex">
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
										</ul>
										<p>Hotel Services</p>
										<ul class="list-unstyled d-flex">
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
										</ul>
										<button class="btn btn-light">Details</button>
									</div>
								</div>
							</div>
						</div>
					</div>
					<div class="col-lg-6 col-12 mb-5">
						<div class="card">
							<div class="row  align-items-center">
								<div class="col-lg-5 col-12 p-0">
									<img
										class="card-img-top"
										src="img/safari2.jpg"
										alt=""
									/>
								</div>
								<div class="col-lg-7 col-12">
									<div class="card-body p-0">
										<h3 class="font-weight-bold">
											Will The Democrats Be Able To Reverse The
											Online Gambling Ban
										</h3>
										<ul class="list-unstyled d-flex">
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
										</ul>
										<p>Hotel Services</p>
										<ul class="list-unstyled d-flex">
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
										</ul>
										<button class="btn btn-light">Details</button>
									</div>
								</div>
							</div>
						</div>
					</div>
					<div class="col-lg-6 col-12 mb-5">
						<div class="card">
							<div class="row  align-items-center">
								<div class="col-lg-5 col-12 p-0">
									<img
										class="card-img-top"
										src="img/safari3.jpg"
										alt=""
									/>
								</div>
								<div class="col-lg-7 col-12">
									<div class="card-body p-0">
										<h3 class="font-weight-bold">
											Get Around Easily With A New York Limousine
											Service
										</h3>
										<ul class="list-unstyled d-flex">
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
										</ul>
										<p>Hotel Services</p>
										<ul class="list-unstyled d-flex">
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
										</ul>
										<button class="btn btn-light">Details</button>
									</div>
								</div>
							</div>
						</div>
					</div>
					<div class="col-lg-6 col-12 mb-5">
						<div class="card">
							<div class="row  align-items-center">
								<div class="col-lg-5 col-12 p-0">
									<img
										class="card-img-top"
										src="img/safari4.jpg"
										alt=""
									/>
								</div>
								<div class="col-lg-7 col-12">
									<div class="card-body p-0">
										<h3 class="font-weight-bold">
											See The Unmatched Beauty Of The Great Lakes
										</h3>
										<ul class="list-unstyled d-flex">
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-star text-main"
													aria-hidden="true"
												></i>
											</li>
										</ul>
										<p>Hotel Services</p>
										<ul class="list-unstyled d-flex">
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
											<li>
												<i
													class="fas mr-2 fa-2x fa-hotel"
													aria-hidden="true"
												></i>
											</li>
										</ul>
										<button class="btn btn-light">Details</button>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</section>
		<!-- end section recomends -->

		<!-- start section partners -->
		<section class="partners py-6 ">
			<div class="container">
				<h1 class="font-weight-bold">Our Partners</h1>

				<div class="partners__images row justify-content-center py-7">
					<div class="col- mr-4 mb-3">
						<img src="img/aman.png"  class="img-fluid" alt="" />
					</div>
					<div class="col- mr-4 mb-3">
						<img src="img/fawry-en.png" class="img-fluid"  alt="" />
					</div>
					<div class="col- mr-4 mb-3">
						<img src="img/enactus.png" class="img-fluid"  alt="" />
					</div>
					<div class="col- mr-4 mb-3">
						<img src="img/adidas.png" class="img-fluid"  alt="" />
					</div>
					<div class="col- mr-4 mb-3">
						<img src="img/Visa.png" class="img-fluid"  alt="" />
					</div>
				</div>
			</div>
		</section>
		<!-- end section partners -->

		<!-- start section travel -->
		<section class="travel py-6">
			<div class="container">
				<div class="row no-gutters justify-content-between">
					<h2 class="font-weight-bold">Travel blog</h2>
					<nav>
						<div class="nav nav-tabs" id="nav-tab" role="tablist">
							<a
								class="nav-link active"
								id="nav-home-tab"
								data-toggle="tab"
								href="#combo"
								role="tab"
								aria-controls="nav-home"
								aria-selected="true"
								>Review</a
							>
							<a
								class="nav-link"
								id="nav-profile-tab"
								data-toggle="tab"
								href="#hotels"
								role="tab"
								aria-controls="nav-profile"
								aria-selected="false"
								>Destination</a
							>
							<a
								class="nav-link"
								id="nav-home-tab"
								data-toggle="tab"
								href="#combo"
								role="tab"
								aria-controls="nav-home"
								aria-selected="true"
								>handbook</a
							>
						</div>
					</nav>
					<h5 class="mt-3">View all</h5>
				</div>

				<div class="row py-5">
					<div class="col-lg-3 col-md-6 col-12">
						<div class="travel__card card-shadowed d-block">
							<img
								class="card-img-bottom"
								src="img/blog1.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1">
								<h5 class="font-weight-bold">
									From Wetlands To Canals And Dams Amsterdam Is Alive
								</h5>
								<p>
									Global Resorts Network Grn Putting Timeshares To
									Shame
								</p>
							</div>
						</div>
					</div>
					<div class="col-lg-3 col-md-6 col-12">
						<div class="travel__card card-shadowed d-block">
							<img
								class="card-img-bottom"
								src="img/blog2.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1">
								<h5 class="font-weight-bold">
									Cost Cutting Ideas For Your Wedding
								</h5>
								<p>
									Travel Health Useful Medical Information For Good
									Health Be
								</p>
							</div>
						</div>
					</div>
					<div class="col-lg-3 col-md-6 col-12">
						<div class="travel__card card-shadowed d-block">
							<img
								class="card-img-bottom"
								src="img/blog4.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1">
								<h5 class="font-weight-bold">
									Getting Cheap Airfare For Last Minute Travel
								</h5>
								<p>Family Safari Vacation To The Home Of The Gods</p>
							</div>
						</div>
					</div>
					<div class="col-lg-3 col-md-6 col-12">
						<div class="travel__card card-shadowed d-block">
							<img
								class="card-img-bottom"
								src="img/blog3.jpg"
								alt="Card image cap"
							/>
							<div class="card-body p-1">
								<h5 class="font-weight-bold">
									New Ideas For A Low Cost Vacation On Water
								</h5>
								<p>
									Will The Democrats Be Able To Reverse The Online
									Gambling Ban
								</p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</section>
		<!-- end section travel -->
	</div>

	<!-- end header section -->
</template>

<script>
import Slick from "vue-slick";
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios,axios)
export default {
	components: {
		Slick,
	},
	data(){
		return {list:undefined};

    },
	mounted() {
		console.log("mounted");
		Vue.axios.get('https://task.shopzad.com/api/products')
        .then((resp)=>{
            this.list = resp.data;
            console.warn(this.list)
            console.warn(resp);
            console.warn(resp.data);
            console.warn(resp.data.data);
        })
	},
	computed: {
        slickOptions2() {
            return {
                slidesToShow: 5,
                slidesToScroll: 1,
                autoplay: true,
                responsive: [
                    {
                        breakpoint: 1200,
                        settings: {
                            slidesToShow: 5,
                            slidesToScroll: 1,
                        }
                    },
                    {
                        breakpoint: 800,
                        settings: {
                            slidesToShow: 3,
                            slidesToScroll: 1,
                        }
                    },
                    {
                        breakpoint: 500,
                        settings: {
                            slidesToShow: 1,
                            slidesToScroll: 1,
                        }
                    }
                ]}
            }
        },
};


</script>
