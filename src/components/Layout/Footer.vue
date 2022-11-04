<template>
    <div class="footer-section pt-70 pb-40">
        <div class="container">
            <!-- <div class="subscribe-area">
                <div class="row align-items-center">
                    <div class="col-lg-6 col-md-6">
                        <div class="subscribe-content">
                            <h2>Join Our Newsletter</h2>
                            <p>News letter dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>
                        </div>
                    </div>

                    <div class="col-lg-6 col-md-6">
                        <form class="newsletter-form">
                            <input type="email" class="input-newsletter" placeholder="Enter your email" name="EMAIL" required>
                            <button type="submit">
                                Subscribe Now
                            </button>
                        </form>
                    </div>
                </div>
            </div> -->

            <div class="row">
                <div class="col-lg-3 col-md-6 col-sm-6">
                    <div class="single-footer-widget">
                        <div class="footer-heading">
                            <h3>Acerca de nosotros</h3>
                        </div>
                        <p>
                            En Laboratorios Chontalpa proporcionamos servicios auxiliares del diagnóstico médico que garantiza los más altos estándares de calidad para contribuir al cuidado y mejor la salud en la sociedad.
                            Más de 40 años de experiencia respaldan nuestro trabajo.
                        </p>

                        <ul class="footer-social">
                            <li>
                                <a href="https://www.facebook.com/LaboratoriosChontalpa/" target="_blank">
                                    <i class="flaticon-facebook"></i>
                                </a>
                            </li>
                             <!-- <li>
                                <a href="#" target="_blank">
                                    <i class="flaticon-twitter"></i>
                                </a>
                            </li> -->
                            <!-- <li>
                                <a href="#" target="_blank">
                                    <i class="flaticon-pinterest"></i>
                                </a>
                            </li>  -->
                            <li>
                                <a href="#" target="_blank">
                                    <i class="flaticon-instagram"></i>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="col-lg-3 col-md-6 col-sm-6">
                    <div class="single-footer-widget">
                        <div class="footer-heading">
                            <h3></h3>
                        </div>

                        <ul class="footer-quick-links">
                            <li>
                                <router-link to="/nosotros">Nosotros</router-link>
                            </li>
                            <li>
                                <router-link to="/blog">Blog</router-link>
                            </li>
                            <li>
                                <router-link to="/contact">Contacto</router-link>
                            </li>
                        </ul>
                    </div>    
                </div>

                <div class="col-lg-3 col-md-6 col-sm-6">
                    <div class="single-footer-widget">
                        <div class="footer-heading">
                            <h3>Servicios</h3>
                        </div>
                        <ul class="footer-quick-links">
                            <li>
                                <router-link to="/estudios">Estudios</router-link>
                            </li>
                            <li>
                                <router-link to="/capacitacion">Capacitación</router-link>
                            </li>
                            <li>
                                <router-link to="/webinar">Webinar</router-link>
                            </li>
                        </ul>
                    </div>    
                </div>

                <div class="col-lg-3 col-md-6 col-sm-6">
                    <div class="single-footer-widget">
                        <div class="footer-heading">
                            <h3>Contacto</h3>
                        </div>

                        <div class="footer-info-contact">
                            <i class="flaticon-phone-call"></i>
                            <h3>Atención telefónica las 24 horas:</h3>
                            <span><a href="tel:+882-569-756">800 501 55 55</a></span>
                        </div>

                        <div class="footer-info-contact">
                            <i class="flaticon-envelope"></i>
                            <h3>Whatsapp</h3>
                            <span><a href="554 540 0680">554 540 0680</a></span>
                        </div>

                        <!-- <div class="footer-info-contact">
                            <i class="flaticon-pin"></i>
                            <h3>Address</h3>
                            <span>32 st Kilda Road, Melbourne VIC, 3004 Australia</span>
                        </div> -->
                    </div>
                </div>
            </div>
        </div>

        <div class="lines">
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Footer'
    }
</script>