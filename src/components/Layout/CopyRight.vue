<template>
    <div class="copyright-area">
        <div class="container">
            <div class="copyright-area-content">
                <div class="row align-items-center">
                    <div class="col-lg-6 col-md-6">
                        <p>
                            Copyright &copy; {{currentYear}} Lab. Todos los derechos reservados por 
                            <a href="https://www.laboratorioschontalpa.com.mx/" target="_blank">
                                https://www.laboratorioschontalpa.com.mx/
                            </a>
                        </p>
                    </div>

                    <div class="col-lg-6 col-md-6">
                        <ul>
                            <li>
                                <router-link to="/terms-condition">Términos y Condiciones</router-link>
                            </li>
                            <li>
                                <router-link to="/privacy-policy">Aviso de Privacidad</router-link>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CopyRight',
    data() {
        return {
            currentYear: new Date().getFullYear(),
        };
    }
}
</script>