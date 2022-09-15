<template>
    <div>
        <Navbar />
        <PageTitle />
        <Services />
        <Footer />
        <CopyRight />
    </div>
</template>

<script>
    import Navbar from '../Layout/Navbar'
    import PageTitle from '../Capacitacion/PageTitle'
    import Services from '../Capacitacion/Services'
    import Footer from '../Layout/Footer'
    import CopyRight from '../Layout/CopyRight'

    export default {
        name: 'Capacitacion',
        components: {
            Navbar,
            PageTitle,
            Services,
            Footer,
            CopyRight,
        }
    }
</script>