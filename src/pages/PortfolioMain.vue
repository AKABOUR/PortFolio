<script setup>
    import PageTitle from '@/components/PageTitle.vue';
    import Biographie from '@/components/Biographie.vue';
    import MesCompetences from '@/components/MesCompetences.vue';
    import MesXp from '@/components/MesXp.vue';
    import MesFormations from '@/components/MesFormations.vue';
    import MesLoisires from '@/components/MesLoisires.vue';
    import Footer from '@/components/Footer.vue';
</script>

<template>
    <div>
        <PageTitle />
        <Biographie />
        <MesFormations />
        <MesCompetences />
        <MesXp />
        <MesLoisires />
        <Footer />
    </div>
</template>

<style scoped>

</style>