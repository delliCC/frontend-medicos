<template>
    <div>
        <Navbar />
        <PageTitle />
        <Protfolio />
        <Footer />
        <CopyRight />
    </div>
</template>

<script>
    import Navbar from '../Layout/Navbar'
    import PageTitle from '../Estudios/PageTitle'
    import Protfolio from '../Estudios/Protfolio'
    import Footer from '../Layout/Footer'
    import CopyRight from '../Layout/CopyRight'

    export default {
        name: 'Estudios',
        components: {
            Navbar,
            PageTitle,
            Protfolio,
            Footer,
            CopyRight,
        }
    }
</script>