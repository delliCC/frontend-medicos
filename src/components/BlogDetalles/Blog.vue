<template>
    <div class="blog-section pt-100 pb-100">
        <div class="container">
            <div class="row">
                <div class="col-lg-8 col-md-12">
                    <div class="blog-details-desc">
                        <div class="article-image">
                            <img :src="`${imagen_destacada}`"  alt="image">
                        </div>
                        <div class="article-content">
                            <div class="entry-meta">
                                <ul>
                                    <li>
                                        <span>Publicado el: </span>
                                        <span v-text="`${fecha}`"></span>
                                    </li>
                                    <!-- <li>
                                        <span>Posted By:</span> 
                                        <router-link to="/">John Anderson</router-link>
                                    </li> -->
                                </ul>
                            </div>

                            <h3 v-text="`${titulo}`"></h3>
                            <p v-text="`${descripcion_portada}`"></p>
                            <!-- <p>Quuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quia non numquam eius modi tempora incidunt ut labore et dolore magnam dolor sit amet, consectetur adipisicing.</p> -->
                            <!-- <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in  sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.</p> -->
                            <blockquote class="wp-block-quote">
                                <p>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.</p>
                                <cite>Tom Cruise</cite>
                            </blockquote>
                            <p v-text="`${descripcion}`"></p>
                            <!-- <p>Quuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quia non numquam eius modi tempora incidunt ut labore et dolore magnam dolor sit amet, consectetur adipisicing.</p> -->
                            <ul class="wp-block-gallery columns-3">
                                <li class="blocks-gallery-item">
                                    <figure>
                                        <img src="../../assets/images/blog/blog-details-4.jpg" alt="image">
                                    </figure>
                                </li>

                                <li class="blocks-gallery-item">
                                    <figure>
                                        <img src="../../assets/images/blog/blog-details-2.jpg" alt="image">
                                    </figure>
                                </li>

                                <li class="blocks-gallery-item">
                                    <figure>
                                        <img src="../../assets/images/blog/blog-details-3.jpg" alt="image">
                                    </figure>
                                </li>
                            </ul>
                            <div style="text-align: center;">
                                <img src="https://laboratorios-chontalpa-file.s3.amazonaws.com/assets/laboratorios-chontalpa-logotipo1.png" alt="avatar">
                                <p style="color: #FF6600;">www.laboratorioschontalpa.com.mx</p>
                                <h4 style="margin: 0px;"> Dra. Adriana Arellano Toriz</h4>
                                <p style="margin: 0px;">Médico especialista en Patología Clínica</p>
                                <p style="margin: 0px;">Cédula de Especialidad: 11507374</p>
                                <p style="margin: 0px;">Jefe de Vinculación Médica Laboratorios Chontalpa</p>
                            </div>
                        </div>

                        <div class="article-footer">
                            <div class="article-tags">
                                <!-- <span>
                                    <i class="bx bx-bookmark"></i>
                                </span>
                                <router-link to="/">Fashion</router-link>,
                                <router-link to="/">Travel</router-link> -->
                            </div> 

                            <div class="article-share">
                                <ul class="social">
                                    <li><span>compartir:</span></li>
                                    <li>
                                        <a href="https://www.facebook.com/LaboratoriosChontalpa/" target="_blank">
                                            <i class="flaticon-facebook"></i>
                                        </a>
                                    </li>
                                    <li>
                                        <a href="#" target="_blank">
                                            <i class="flaticon-instagram"></i>
                                        </a>
                                    </li>
                                </ul>
                            </div>
                        </div>

                        <div class="post-navigation">
                            <div class="navigation-links">
                                <div class="nav-previous">
                                    <router-link to="/">
                                        <i class="flaticon-left"></i> 
                                        Prev Post
                                    </router-link>
                                </div>
                                <div class="nav-next">
                                    <router-link to="/">
                                        Next Post 
                                        <i class="flaticon-right"></i>
                                    </router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-4 col-md-12">
                    <Sidebar />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Sidebar from '../Common/Sidebar'

    export default {
        name: 'Blog',
        components: { 
            Sidebar
        },
        data() {
            return {
                imagen_destacada:null,
                titulo: null,
                fecha: null,
                descripcion_portada: null,
                descripcion: null,
                modalShow: false,
        
            }
        },
        mounted() {
            this.aplicar()
        },
        methods:{
            aplicar(){
                var id = this.$route.params.id;
            
                this.$axios.get(`/blog/datos/${id}`).then(response => {
                    // console.log(response)
                    var blog = response.data.data
                    this.imagen_destacada = blog.imagen_destacada
                    this.titulo = blog.titulo
                    this.fecha = blog.fecha
                    this.descripcion_portada = blog.descripcion_portada
                    this.descripcion = blog.descripcion
                    console.log(this.imagen_destacada )
                //     this.datosPostulante.puesto_id = vacante.puesto_id
                //     this.datosPostulante.sucursal_id = vacante.sucursal_id
                    
                //     this.datosPostulante.puesto_solicitado = vacante.puesto.puesto
                //     this.datosPostulante.sucursal = vacante.sucursal.sucursal
                })
            },
        }
    }
</script>