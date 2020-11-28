<template>
    <div class="about">
        <!-- Start main slider -->
        <section class="main-slider py-6 mb-3">
            <div class="container">
                <div class="row no-gutters mt-8">
                    <h5 class="text-main mr-2">Hotels</h5>
                    <h5 class="secondry-color">Family Safari Vacation To The Home Of The Gods</h5>
                </div>
            </div>
            
            <Slick class="slider-arrows-circle-light" data-provide="slider" data-arrows="true" data-dots="true">
                <div><img src="img/promotion1.jpg"></div>
                <div><img src="img/promotion2.jpg"></div>
                <div><img src="img/promotion3.jpg"></div>
            </Slick>
        </section>
        <!-- Start main slider -->

        <!-- start booking details -->
        <section class="booking-details py-2">
            <div class="container">
                <div class="main row my-3">
                    <div class="col-lg-8 col-md-12 col-sm-12">
                        <h1>Family Safari Vacation To The Home Of The Gods</h1>
                        <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic</p>
                        <Slick ref="c1" :autoplay="true" :asNavFor="$refs.c2" :focusOnSelect="true" class="slider-arrows-circle-light slickslider" id="slider-image" data-provide="slider" data-as-nav-for="#slider-thumb" data-arrows="true">
                            <div class="p-2"><img src="img/safari1.jpg"></div>
                            <div class="p-2"><img src="img/safari2.jpg"></div>
                            <div class="p-2"><img src="img/safari3.jpg"></div>
                            <div class="p-2"><img src="img/safari4.jpg"></div>
                        </Slick>

                        <Slick ref="c2" :autoplay="true" :asNavFor="$refs.c1" :slidesToShow="6" :focusOnSelect="true" class="slider-arrows-circle-light small-slider">
                            <div class="p-2"><img class="cursor-pointer" src="img/safari1.jpg"></div>
                            <div class="p-2"><img class="cursor-pointer" src="img/safari2.jpg"></div>
                            <div class="p-2"><img class="cursor-pointer" src="img/safari3.jpg"></div>
                            <div class="p-2"><img class="cursor-pointer" src="img/safari4.jpg"></div>
                            <div class="p-2"><img class="cursor-pointer" src="img/safari5.jpg"></div>
                            <div class="p-2"><img class="cursor-pointer" src="img/safari6.jpg"></div>
                            <div class="p-2"><img class="cursor-pointer" src="img/safari7.jpg"></div>
                        </Slick>
                    </div>

                    <div class="col-lg-4 col-md-12 col-sm-12">
                        <div class="card border-1">
                            <div class="row bg-dark no-gutters p-2">
                                <div class="col-12">
                                    <h4 class="text-white">Book your room now</h4>
                                </div>
                            </div>
                            <div class="row p-3">
                                <div class="col-12">
                                    <h4>Tourist Information</h4>
                                </div>
                                <div class="col-12">
                                    <h5>Nationality</h5>
                                </div>
                                <div class="col-6">
                                    <button class="btn btn-main">local Team</button>
                                </div>
                                <div class="col-6">
                                    <button class="btn btn-light">Foreign Tourist</button>
                                </div>
                                <div class="col-lg-6">
                                    <div class="form-group">
                                        <label for="checkin">Check-in</label>
                                        <input id="check-in" class="form-control" type="text" name="check-in">
                                    </div>
                                </div>
                                <div class="col-lg-6">
                                    <div class="form-group">
                                        <label for="time">Time</label>
                                        <select class="form-control" name="" id="">
                                            <option value="">1:30 AM</option>
                                            <option value="">1:30 AM</option>
                                            <option value="">1:30 AM</option>
                                        </select>
                                    </div>
                                </div>
                                <div class="col-lg-6">
                                    <div class="form-group">
                                        <label for="checkout">Check-out</label>
                                        <input id="checkout" class="form-control" type="date" name="checkout">
                                    </div>
                                </div>
                                <div class="col-lg-6">
                                    <div class="form-group">
                                        <label for="time">Time</label>
                                        <select class="form-control" name="" id="">
                                            <option value="">1:30 AM</option>
                                            <option value="">1:30 AM</option>
                                            <option value="">1:30 AM</option>
                                        </select>
                                    </div>
                                </div>
                                <div class="col-12">
                                    <h1 class="font-weight-bold">Contact information</h1>
                                </div>
                                <div class="col-12">
                                    <div class="form-group">
                                        <label for="firstname">First and last name: <span class="text-danger">*</span></label>
                                        <input id="firstname" class="form-control" type="text" name="firstname">
                                    </div>
                                </div>
                                <div class="col-12">
                                    <div class="form-group">
                                        <label for="email">Email: <span class="text-danger">*</span></label>
                                        <input id="email" class="form-control" type="text" name="email">
                                    </div>
                                </div>
                                <div class="col-12">
                                    <div class="form-group">
                                        <label for="phone">Phone Number: <span class="text-danger">*</span></label>
                                        <input id="phone" class="form-control" type="text" name="phone">
                                    </div>
                                </div>
                                <div class="col-12">
                                    <button class="btn btn-main btn-block">Book now</button>
                                </div>
                            </div>
                        </div>
                        
                    </div>
                </div>
            </div>
        </section>
        <!-- end booking details -->

        <!-- Start service details -->
        <section class="service-details">
            <div class="container">
                <div class="row">
                    <div class="col-lg-8 col-12 mb-5">
                        <h1 class="font-weight-bold">GUESTS SERVICES OF SUN TRAVEL</h1>
                        <p>Reservation and ticketing by phone, email from 8:00 to 18:30 on weekdays (including Holidays and New Year).
                        Free ticket delivery in the city.
                        Free advice on the best flight routes with the most suitable price.
                        Advice on participation and benefit from frequent flyer programs of airlines such as: Golden Lotus Plus, Asia Miles, Royal Orchid Plus ...
                        Support changing date, time of flight, refund tickets quickly and conveniently.</p>
                    </div>
                    <div class="col-lg-8 col-12 mb-5">
                        <h1 class="font-weight-bold">GUESTS SERVICES OF SUN TRAVEL</h1>
                        <p>Reservation and ticketing by phone, email from 8:00 to 18:30 on weekdays (including Holidays and New Year).
                        Free ticket delivery in the city.
                        Free advice on the best flight routes with the most suitable price.
                        Advice on participation and benefit from frequent flyer programs of airlines such as: Golden Lotus Plus, Asia Miles, Royal Orchid Plus ...
                        Support changing date, time of flight, refund tickets quickly and conveniently.</p>
                    </div>
                    <div class="col-lg-8 col-12 mb-9">
                        <h1 class="font-weight-bold">GUESTS SERVICES OF SUN TRAVEL</h1>
                        <p>Reservation and ticketing by phone, email from 8:00 to 18:30 on weekdays (including Holidays and New Year).
                        Free ticket delivery in the city.
                        Free advice on the best flight routes with the most suitable price.
                        Advice on participation and benefit from frequent flyer programs of airlines such as: Golden Lotus Plus, Asia Miles, Royal Orchid Plus ...
                        Support changing date, time of flight, refund tickets quickly and conveniently.</p>
                    </div>
                </div>
            </div>
        </section>
        <!-- end service details -->

        <!-- Start section similarity -->
        <section class="similar-hotels">
            <div class="container">
                <div class="row">
                    <div class="col-lg-3 col-md-6 col-12">
                        <div class="card d-block">
                            <img class="card-img-top" src="img/safari1.jpg" alt="Card image cap">
                            <div class="card-body p-0">
                                <h5 class="card-title font-weight-bold">From Wetlands To Canals And Dams Amsterdam Is Alive</h5>
                                <p>Travel Health Useful Medical Information For Good Health Be</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-3 col-md-6 col-12">
                        <div class="card d-block">
                            <img class="card-img-top" src="img/safari2.jpg" alt="Card image cap">
                            <div class="card-body p-0">
                                <h5 class="card-title font-weight-bold">Cost Cutting Ideas For Your Wedding</h5>
                                <p>Global Resorts Network Grn Putting Timeshares To Shame</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-3 col-md-6 col-12">
                        <div class="card d-block">
                            <img class="card-img-top" src="img/safari3.jpg" alt="Card image cap">
                            <div class="card-body p-0">
                                <h5 class="card-title font-weight-bold">Getting Cheap Airfare For Last Minute Travel</h5>
                                <p>Family Safari Vacation To The Home Of The Gods</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-3 col-md-6 col-12">
                        <div class="card d-block">
                            <img class="card-img-top" src="img/safari4.jpg" alt="Card image cap">
                            <div class="card-body p-0">
                                <h5 class="card-title font-weight-bold">New Ideas For A Low Cost Vacation On Water</h5>
                                <p>Will The Democrats Be Able To Reverse The Online Gambling Ban</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- end section similarity -->
    </div>
</template>
<script>
import Slick from 'vue-slick-carousel';

export default {
    components:{
        Slick
    },
    mounted() {
        console.log("mounted")
    },
}
</script>