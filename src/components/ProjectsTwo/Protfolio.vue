<template>
    <div class="protfolio-section ptb-100">
        <div class="container">
            <div class="section-title">
                <h2>Nuestros <span>estudios</span></h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incidiunt labore et dolore magna aliqua. Quis ipsum suspendisse ultrices gravida.</p>
                <div class="bar"></div>
            </div>

            <div class="row">
                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-protfolio">
                        <div class="image">
                            <router-link to="/estudios-detalle">
                                <img src="../../assets/images/portfolio/portfolio-1.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/estudios-detalle">
                                <h3>Creative Web Develop</h3>
                            </router-link>
                            <router-link to="/estudios-detalle">
                                <span>Web Design</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-protfolio">
                        <div class="image">
                            <router-link to="/estudios-detalle">
                                <img src="../../assets/images/portfolio/portfolio-2.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/estudios-detalle">
                                <h3>Digital Services</h3>
                            </router-link>
                            <router-link to="/estudios-detalle">
                                <span>App Development</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-protfolio">
                        <div class="image">
                            <router-link to="/estudios-detalle">
                                <img src="../../assets/images/portfolio/portfolio-3.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/estudios-detalle">
                                <h3>Complex Design</h3>
                            </router-link>
                            <router-link to="/estudios-detalle">
                                <span>Software Development</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-protfolio">
                        <div class="image">
                            <router-link to="/estudios-detalle">
                                <img src="../../assets/images/portfolio/portfolio-4.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/estudios-detalle">
                                <h3>Creative Web Develop</h3>
                            </router-link>
                            <router-link to="/estudios-detalle">
                                <span>React Development</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-protfolio">
                        <div class="image">
                            <router-link to="/estudios-detalle">
                                <img src="../../assets/images/portfolio/portfolio-5.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/estudios-detalle">
                                <h3>Digital Services</h3>
                            </router-link>
                            <router-link to="/estudios-detalle">
                                <span>E-commerce Development</span>
                            </router-link>
                        </div>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-protfolio">
                        <div class="image">
                            <router-link to="/estudios-detalle">
                                <img src="../../assets/images/portfolio/portfolio-6.png" alt="image">
                            </router-link>
                        </div>

                        <div class="content">
                            <router-link to="/estudios-detalle">
                                <h3>Complex Design</h3>
                            </router-link>
                            <router-link to="/estudios-detalle">
                                <span>Software Engineering</span>
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
        name: 'Protfolio',
        data() {
            return {
                
            }
        },
        mounted() {
            this.estudios()
        },
        methods:{
            estudios(ctx, callback) {
                this.$axios.get('http://localhost/api/estudios', {
                    // params: {
                    // page: ctx.currentPage,
                    // filter: ctx.filter,
                    // sortBy: ctx.sortBy,
                    // sortDesc: ctx.sortDesc ? 'desc' : 'asc',
                    // perPage: ctx.perPage,
                    // },
                }).then(response => {
                    console.log(response)
                    const res = response.data.data
                    console.log(res)
                    // const clientes = res.data.map(element => ({
                    // id: element.id,
                    // ax_ceros: element.ax_ceros,
                    // codigo_stw: element.codigo_stw,
                    // nombre_cliente: element.nombre_cliente,
                    // status: element.status ? 'Activo' : 'Inactivo',
                    // }))
                    // this.totalRows = res.total
                    // this.tableTo = res.to
                    // this.tableFrom = res.from
                    callback()
                }).catch(() => {
                    //localStorage.removeItem('usuario_cobranza')
                })
            },
        }
    }
</script>