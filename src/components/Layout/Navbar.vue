<template>
    <div>
        <div :class="['navbar-area', {'is-sticky': isSticky}]">
            <div class="valzo-nav">
                <div class="container">
                    <nav class="navbar navbar-expand-lg navbar-light">
                        <router-link class="navbar-brand" to="/">
                            <!-- <img src="https://laboratorios-chontalpa-file.s3.amazonaws.com/assets/favicon.png" alt="avatar" > -->
                            <img src="https://laboratorios-chontalpa-file.s3.amazonaws.com/assets/laboratorios-chontalpa-logotipo1.png" alt="avatar">
                            <!-- <img src="../../assets/images/logo.png" alt="logo"> -->
                        </router-link>

                        <div 
                            class="navbar-toggler"
                            @click="active = !active" :aria-pressed="active ? 'true' : 'false'"
                            v-bind:class="{ 'active': button_active_state }"
                            v-on:click="button_active_state = !button_active_state"
                        >
                            <span class="icon-bar top-bar"></span>
                            <span class="icon-bar middle-bar"></span>
                            <span class="icon-bar bottom-bar"></span>
                        </div>

                        <div class="collapse navbar-collapse" :class="{ show: active }" is-nav>
                            <ul class="navbar-nav">
                                <li class="nav-item">
                                    <a href="#" class="nav-link">
                                        Inicio 
                                        <!-- <i class='bx bx-chevron-down'></i> -->
                                    </a>
                                    <!-- <ul class="dropdown-menu">
                                        <li class="nav-item">
                                            <router-link  to="/" class="nav-link">
                                                Home One
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/home-two" class="nav-link">
                                                Home Two
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/home-three" class="nav-link">
                                                Home Three
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/home-four" class="nav-link">
                                                Home Four
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/home-five" class="nav-link">
                                                Home Five
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/home-six" class="nav-link">
                                                Home Six
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/home-seven" class="nav-link">
                                                Home Seven
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/home-eight" class="nav-link">
                                                Home Eight
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/home-nine" class="nav-link">
                                                Home Nine
                                            </router-link>
                                        </li>
                                    </ul> -->
                                </li>

                                <li class="nav-item">
                                    <router-link  to="/nosotros" class="nav-link">
                                        Nosotros
                                    </router-link>
                                </li>

                                <li class="nav-item">
                                    <a href="#" class="nav-link">
                                        Cursos 
                                        <i class='bx bx-chevron-down'></i>
                                    </a>
                                    <ul class="dropdown-menu">
                                        <li class="nav-item">
                                            <router-link  to="/capacitacion" class="nav-link">
                                                Capacitación
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/webinar" class="nav-link">
                                                Webinar
                                            </router-link>
                                        </li>

                                        <!-- <li class="nav-item">
                                            <router-link  to="/single-services" class="nav-link">
                                                Services Details
                                            </router-link>
                                        </li> -->
                                    </ul>
                                </li>

                                <li class="nav-item">
                                    <router-link  to="/estudios" class="nav-link">
                                        Estudios
                                    </router-link>
                                    <!-- <a href="#" class="nav-link">
                                        Projects 
                                        <i class='bx bx-chevron-down'></i>
                                    </a>

                                    <ul class="dropdown-menu">
                                        <li class="nav-item">
                                            <router-link  to="/projects-one" class="nav-link">
                                                Projects One
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/projects-two" class="nav-link">
                                                Projects Two
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/single-projects" class="nav-link">
                                                Projects details
                                            </router-link>
                                        </li>
                                    </ul> -->
                                </li>

                                <!-- <li class="nav-item">
                                    <a href="#" class="nav-link">
                                        Pages 
                                        <i class='bx bx-chevron-down'></i>
                                    </a>

                                    <ul class="dropdown-menu">
                                        <li class="nav-item">
                                            <router-link  to="/about" class="nav-link">
                                                About
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/team" class="nav-link">
                                                Team
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/pricing" class="nav-link">
                                                Pricing
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/faq" class="nav-link">
                                                FAQ
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <a href="#" class="nav-link">
                                                User 
                                                <i class='bx bx-chevron-down'></i>
                                            </a>

                                            <ul class="dropdown-menu">
                                                <li class="nav-item">
                                                    <router-link  to="/log-in" class="nav-link">
                                                        Log In
                                                    </router-link>
                                                </li>

                                                <li class="nav-item">
                                                    <router-link  to="/sign-up" class="nav-link">
                                                        Sign Up
                                                    </router-link>
                                                </li>
                                            </ul>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/terms-condition" class="nav-link">
                                                Terms & Conditions
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/privacy-policy" class="nav-link">
                                                Privacy Policy
                                            </router-link>
                                        </li>
                                    
                                        <li class="nav-item">
                                            <router-link  to="/error-404" class="nav-link">
                                                404 Error
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/contact" class="nav-link">
                                                Contact
                                            </router-link>
                                        </li>
                                    </ul>
                                </li> -->

                                <li class="nav-item">
                                    <router-link  to="/blog-one" class="nav-link">
                                        Blog
                                    </router-link>
                                    <!-- <a href="#" class="nav-link">
                                        Blog 
                                        <i class='bx bx-chevron-down'></i>
                                    </a>
                                    <ul class="dropdown-menu">
                                        <li class="nav-item">
                                            <router-link  to="/blog-one" class="nav-link">
                                                Blog Grid
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/blog-two" class="nav-link">
                                                Blog Right Sidebar
                                            </router-link>
                                        </li>

                                        <li class="nav-item">
                                            <router-link  to="/single-blog" class="nav-link">
                                                Blog Details
                                            </router-link>
                                        </li>
                                    </ul> -->
                                </li>

                                <li class="nav-item">
                                    <router-link  to="/contact" class="nav-link">
                                        Contacto
                                    </router-link>
                                </li>
                                <li class="nav-item">
                                    <router-link  to="/log-in" class="nav-link">
                                        Iniciar sesión
                                    </router-link>
                                </li>
                            </ul>
                        </div>

                        <!-- icono  -->
                        <!-- <div class="others-options">
                            <div 
                                class="burger-menu"
                                v-on:click="isPopupMethod(isPopup)"
                            >
                                <span></span>
                                <span></span>
                                <span></span>
                            </div>
                        </div> -->
                    </nav>
                </div>
            </div>
        </div>

        <div 
            class="sidebar-modal"
            v-if="isPopup"
        >
            <div class="sidebar-modal-inner">
                <div class="sidebar-about">
                    <div class="title">
                        <h2>About Us</h2>
                        <p>We believe brand interaction is key to communication. Real innovations and positive customer experience are the heart of successful communication. No fake products and services. The customer is king, their lives and needs are the inspiration.</p>
                    </div>
                    <div 
                        class="close-btn"
                        v-on:click="isPopupMethod(isPopup)"
                    >
                        <i class='bx bx-x'></i>
                    </div>
                </div>

                <div class="sidebar-contact-feed">
                    <h2>Contact</h2>
                    <div class="contact-form">
                        <form>
                            <div class="col-lg-12 col-md-12">
                                <div class="send-btn">
                                    <button type="submit" class="send-btn-one">
                                        Send Message
                                    </button>
                                </div>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Navbar',
    data(){
        return {
            isSticky: false,
            isPopup: false,
            active: false,
            button_active_state: false
        }
    },
    methods: {
        isPopupMethod(isPopup){
            return this.isPopup = !isPopup
        },
    },
    mounted(){
        const that = this
        window.addEventListener('scroll', () => {
            let scrollPos = window.scrollY
            if(scrollPos >= 100){
                that.isSticky = true
            } else {
                that.isSticky = false
            }
        })
    }
}
</script>