<template>
    <div class="services-section pt-100 pb-100">
        <div class="container">
            <div class="section-title">
                <h2>Capacitación</h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incidiunt  labore et dolore magna aliqua. Quis ipsum suspendisse ultrices gravida.</p>
                <div class="bar"></div>
            </div>

            <div class="row">
                <div class="col-lg-4 col-md-6" v-for="capacitacion in array_capacitacion" :key="capacitacion.id">
                    <div class="single-services">
                        <div class="icon">
                            <i class="flaticon-it"></i>
                        </div>
                        <h3>{{capacitacion.nombre}}</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore facilisis.</p>
                        <router-link to="/single-services" class="read-btn">Read More</router-link>
                    </div>
                </div>

                <!-- <div class="col-lg-4 col-md-6">
                    <div class="single-services">
                        <div class="icon">
                            <i class="flaticon-setting"></i>
                        </div>
                        <h3>Web Development</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore facilisis.</p>
                        <router-link to="/single-services" class="read-btn">Read More</router-link>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6">
                    <div class="single-services">
                        <div class="icon">
                            <i class="flaticon-promotion"></i>
                        </div>
                        <h3>Digital Marketing</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore facilisis.</p>
                        <router-link to="/single-services" class="read-btn">Read More</router-link>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6">
                    <div class="single-services">
                        <div class="icon">
                            <i class="flaticon-cellphone"></i>
                        </div>
                        <h3>App Development</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore facilisis.</p>
                        <router-link to="/single-services" class="read-btn">Read More</router-link>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6">
                    <div class="single-services">
                        <div class="icon">
                            <i class="flaticon-shopping-cart"></i>
                        </div>
                        <h3>E-commerce Development</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore facilisis.</p>
                        <router-link to="/single-services" class="read-btn">Read More</router-link>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6">
                    <div class="single-services">
                        <div class="icon">
                            <i class="flaticon-optimize"></i>
                        </div>
                        <h3>IT Solutions</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore facilisis.</p>
                        <router-link to="/single-services" class="read-btn">Read More</router-link>
                    </div>
                </div> -->

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

        <div class="default-shape">
            <div class="shape-1">
                <img src="../../assets/images/shapes/shape-4.png" alt="image">
            </div>

            <div class="shape-2 rotateme">
                <img src="../../assets/images/shapes/shape-5.svg" alt="image">
            </div>

            <div class="shape-3">
                <img src="../../assets/images/shapes/shape-6.svg" alt="image">
            </div>

            <div class="shape-4">
                <img src="../../assets/images/shapes/shape-7.png" alt="image">
            </div>

            <div class="shape-5">
                <img src="../../assets/images/shapes/shape-8.png" alt="image">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Services',
        data() {
            return {
                array_capacitacion:[]
            }
        },
        mounted() {
            this.webinar()
        },
        methods:{
            webinar() {
                this.$axios.get(`http://localhost/api/training`).then(response => {
                    this.array_capacitacion = response.data.data
                    console.log(this.array_capacitacion)
                    
                }).catch(() => {
                // this.$toast({
                // component: ToastificationContent,
                // props: {
                //     title: 'Error al cargar datos',
                //     icon: 'ThumbsDownIcon',
                //     variant: 'danger',
                // },
                // })
                })
            },
        }
    }
</script>