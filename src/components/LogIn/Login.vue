<template>
    <div class="login-section ptb-100">
        <div class="container">
            <div class="login-form">
                <div class="login-title">
                    <a href="javascript:void(0);" class="brand-logo">
                        <img src="https://laboratorios-chontalpa-file.s3.amazonaws.com/assets/laboratorios-chontalpa-logotipo1.png" alt="">
                    </a>
                    <h3>PORTAL MÉDICO</h3>
                    <p>Inicia sesión en tu cuenta y comienza la aventura</p>
                </div>
                    
                <form>
                    <div class="row">
                        <div class="col-lg-12">
                            <div class="form-group">
                                <input type="email" class="form-control" placeholder="Email">
                            </div>
                        </div>

                        <div class="col-lg-12">
                            <div class="form-group">
                                <input type="password" class="form-control" placeholder="Password">
                            </div>
                        </div>

                        <div class="col-lg-12">
                            <div class="form-check">
                                <input type="checkbox" class="form-check-input" id="checkme">
                                <label class="form-check-label" for="checkme">Recuérdame</label>
                            </div>
                        </div>

                        <div class="col-lg-12 text-right">
                            <p class="forgot-password"><a href="#">¿Olvidaste tu contraseña?</a></p>
                        </div>

                        <div class="col-lg-12">
                            <div class="send-btn">
                                <button type="submit" class="default-btn">
                                    Inicia sesión
                                    <span></span>
                                </button>
                            </div>
                            <br>
                            <span>¿No tienes cuenta? <router-link to="/sign-up">Registrate! </router-link></span>
                        </div>
                    </div>
                </form>
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
        name: 'Login',
        data() {
            return {
                array_login:[]
            }
        },
        mounted() {
            this.iniciarSesion()
        },
        methods:{
            iniciarSesion() {
                this.$axios.post(`http://localhost/api/login`).then(response => {
                    console.log(response.data)
              
                    // this.array_login = response.data.datos

                  
                    // console.log(JSON.parse(JSON.stringify(response.data.data)))
                    // console.log(this.array_login)
                 
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