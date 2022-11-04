<template>
    <div>
        <Navbar />
        <PageTitle />
        <ProjectDetails />
        <Footer />
        <CopyRight />
    </div>
</template>

<script>
    import Navbar from '../Layout/Navbar'
    import PageTitle from '../EstudiosDetalle/PageTitle'
    import ProjectDetails from '../EstudiosDetalle/ProjectDetails'
    import Footer from '../Layout/Footer'
    import CopyRight from '../Layout/CopyRight'

    export default {
        name: 'SingleProjectsPage',
        components: {
            Navbar,
            PageTitle,
            ProjectDetails,
            Footer,
            CopyRight,
        }
    }
</script>