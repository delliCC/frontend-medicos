<template>
    <div>
        <Navbar />
        <PageTitle />
        <AgencyServices />
        <Footer />
        <CopyRight />
    </div>
</template>

<script>
    import Navbar from '../Layout/Navbar'
    import PageTitle from '../Webinar/PageTitle'
    import AgencyServices from '../Webinar/AgencyServices'
    import Footer from '../Layout/Footer'
    import CopyRight from '../Layout/CopyRight'

    export default {
        name: 'Webinar',
        components: {
            Navbar,
            PageTitle,
            AgencyServices,
            Footer,
            CopyRight,
        }
    }
</script>