<template>
    <div class="agency-services-section pt-100 pb-100">
        <div class="container">
            <div class="section-title">
                <h2>Nuestros  <span>webinar</span></h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incidiunt  labore et dolore magna aliqua. Quis ipsum suspendisse ultrices gravida.</p>
                <div class="bar"></div>
            </div>

            <div class="row">
                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-agency">
                        <div class="image">
                            <router-link to="/webinar-detalle">
                                <img src="https://laboratorios-chontalpa-file.s3.amazonaws.com/webinar1.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/webinar-detalle">
                                <h6>Ventajas del examen de orina por citometria de flujo vs metodos tradicionales</h6>
                            </router-link>
                            <router-link to="/webinar-detalle">
                                <span>Registrarse</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-agency">
                        <div class="image">
                            <router-link to="/webinar-detalle">
                                <img src="../../assets/images/agency/agency-2.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/webinar-detalle">
                                <h6>Repercusiones del sindrome metabolico durante el embarazo</h6>
                            </router-link>
                            <router-link to="/webinar-detalle">
                                <span>Registrarse</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-agency">
                        <div class="image">
                            <router-link to="/webinar-detalle">
                                <img src="../../assets/images/agency/agency-3.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/webinar-detalle">
                                <h3>Complex Design</h3>
                            </router-link>
                            <router-link to="/webinar-detalle">
                                <span>Solutions</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-agency">
                        <div class="image">
                            <router-link to="/webinar-detalle">
                                <img src="../../assets/images/agency/agency-4.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/webinar-detalle">
                                <h3>Software Engineers</h3>
                            </router-link>
                            <router-link to="/webinar-detalle">
                                <span>Analysis</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-agency">
                        <div class="image">
                            <router-link to="/webinar-detalle">
                                <img src="../../assets/images/agency/agency-5.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/webinar-detalle">
                                <h3>Marketing Agency</h3>
                            </router-link>
                            <router-link to="/webinar-detalle">
                                <span>Marketing</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-agency">
                        <div class="image">
                            <router-link to="/webinar-detalle">
                                <img src="../../assets/images/agency/agency-6.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/webinar-detalle">
                                <h3>Data Analysis</h3>
                            </router-link>
                            <router-link to="/webinar-detalle">
                                <span>Explanation</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-12 col-md-12">
                    <div class="pagination-area">
                        <a href="#" class="prev page-numbers">
                            <i class="flaticon-left"></i>
                        </a>
                        <a href="#" class="page-numbers">1</a>
                        <span class="page-numbers current" aria-current="page">2</span>
                        <a href="#" class="page-numbers">3</a>
                        <a href="#" class="page-numbers">4</a>
                        <a href="#" class="next page-numbers">
                            <i class="flaticon-right"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AgencyServices'
    }
</script>