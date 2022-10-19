<template>
    <div>
        <Navbar />
        <PageTitle />
        <Blog />
        <Footer />
        <CopyRight />
    </div>
</template>

<script>
    import Navbar from '../Layout/Navbar'
    import PageTitle from '../BlogDetalles/PageTitle'
    import Blog from '../BlogDetalles/Blog'
    import Footer from '../Layout/Footer'
    import CopyRight from '../Layout/CopyRight'

    export default {
        name: 'SingleBlogPage',
        components: {
            Navbar,
            PageTitle,
            Blog,
            Footer,
            CopyRight,
        },
        data() {
            return {
                imagen_destacada:null,
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
                    console.log(response)
                    var blog = response.data.data
                    this.imagen_destacada = blog.imagen_destacada
                //     this.datosPostulante.puesto_id = vacante.puesto_id
                //     this.datosPostulante.sucursal_id = vacante.sucursal_id
                    
                //     this.datosPostulante.puesto_solicitado = vacante.puesto.puesto
                //     this.datosPostulante.sucursal = vacante.sucursal.sucursal
                })
            },
        }
    }
</script>