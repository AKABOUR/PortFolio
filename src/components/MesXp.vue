<script setup>
    import { ref } from "vue";

    let activeBloc = ref(0)

    let experiences = ref([
    {
        title: "Ingénieur développeur DotNet",
        date: "Depuis septembre 2023",
        line1: "Migration en .NET 8 de toutes la couche service de l'éco-système IsaCompta.",
        line2: "Gestion SAV (Astreintes).",
        line3: "Participation à l'amélioration de l'éco-système IsaCompta."
    },
    {
        title: "Ingénieur développeur DotNet",
        date: "Décembre 2017 - Août 2023",
        line1: "Suivi et maintien des deux portails Web « GidedAgent » et « GidedUSAGER » qui fournissent des services conçus pour répondre aux besoins des collectivités sur la compétence gestion des déchets.",
        line2: "Migration de trois applications mobile vers Angular.",
        line3: "Gestion SAV et formation des internautes.",
        line4: "Interfaçage du portail GidedUsager avec FranceConnect.",
        line5: "Intégration des solutions de paiement en ligne dans le portail GidedUSAGER.",
        line6: "Adaptation et amélioration du module de Facturation des dépôts et enlèvement."
    },
    {
        title: "Chef d’équipe DotNet au sein de YAH Technology ",
        date: "Septembre 2013 - Novembre 2017",
        line1: "Migration de Silverlight vers Asp.Net MVC des deux portail « GidedAgent » et « GidedUSAGER » qui sont deux portails qui fournissent des services conçus pour répondre aux besoins des collectivités sur la compétence gestion des déchets.",
        line2: "Suivi et organisation des travaux d’une équipe de trois développeurs.",
        line3: "Assurer la relation avec notre siège en France « SARL : NETVLM » pour répondre au mieux aux objectifs."
    },
    {
        title: "Ingénieur software confirmé à Creative Technologies",
        date: "Mars 2012 - Juillet 2013",
        line1: "Développement d’un projet d’échantillonnage et de collecte des données pour faire l’enquête de l’emploi du gouvernement du Cap-Vert",
        line2: "Participation à l’analyse des spécifications fonctionnelles (Méthode : Cycle en V) en collaboration avec le chef de projet.",
        line3: "Rédaction de la documentation et formation des internautes."
    },
    {
        title: "Ingénieur Consultant DotNet au sein de la SSII Prestige Informatique",
        date: "Mars 2007 - Février 2012",
        line1: "Projet DocNet pour le compte de l’Office National de l’Eau Potable et le département d’Environnement à Rabat (Maroc)",
        line2: "Projet DocFlow (Gestion de courriers) pour le compte du Crédit Agricole du Maroc, du gouvernement de Mauritanie, du ministère de l’équipement et de transport du Maroc, de Veolia environnement Maroc (VEOM), de Marsa MAROC et d’Amendis Maroc (Tanger et Tétouan).",
        line3: "Projet PhramaNet pour le compte du groupe pharmaceutique SOPHA CENTRE.",
        line4: "Projet de portail « Service Public » pour le compte gouvernement de Mauritanie.",
        line5: "Projet de gestion d’erreurs générées par un serveur IBM pour le compte de la société française TECHNICAL STORAGE."
    }
    ]);

    const ShowXp = (id) => {
        activeBloc.value = id;
    };

</script>

<template>
    <div id="xp">
        <h2 class="text-highlight-1 section-title">Expériences</h2>
        <div id="left">
            <p :class="activeBloc === 0 ? 'active' : ''" class="company fw600" @click="ShowXp(0)">ISAGRI</p>
            <p :class="activeBloc === 1 ? 'active' : ''" class="company fw600" @click="ShowXp(1)">GIDED</p>
            <p :class="activeBloc === 2 ? 'active' : ''" class="company fw600" @click="ShowXp(2)">YAH Technology</p>
            <p :class="activeBloc === 3 ? 'active' : ''" class="company fw600" @click="ShowXp(3)">Créative Technologies</p>
            <p :class="activeBloc === 41 ? 'active' : ''" class="company fw600" @click="ShowXp(4)">Prestige Informatique</p>
        </div>
        <div id="right">
            <template v-for="(job,index) in experiences">
                <div class="job-details" :class="index === activeBloc ? '' : 'hide'" :id="'bloc_'+index">
                    <h3 class="fw600">{{ job.title }}</h3>
                    <span id="date">{{ job.date }}</span>
                    <br/>
                    <p class="fw600 mtb8" style="margin-top: 10px;"><span class="text-highlight-2">✓</span> {{ job.line1 }}</p>
                    <p class="fw600 mtb8"><span class="text-highlight-2">✓</span> {{ job.line2 }}</p>
                    <p class="fw600 mtb8"><span class="text-highlight-2">✓</span> {{ job.line3 }}</p>
                    <p class="fw600 mtb8" v-if="job.line4 != null"><span class="text-highlight-2">✓</span> {{ job.line4 }}</p>
                    <p class="fw600 mtb8" v-if="job.line5 != null"><span class="text-highlight-2">✓</span> {{ job.line5 }}</p>
                    <p class="fw600 mtb8" v-if="job.line6 != null"><span class="text-highlight-2">✓</span> {{ job.line6 }}</p>
                </div>
            </template>
        </div>
    </div>
</template>

<style scoped>
    #xp {
        margin-top: 60px;
    }

    #xp #left {
        float: left;
        width: 25%;
    }

    #xp::after {
  content: "";
  display: table;
  clear: both;
}

    #xp #right {
        float: left;
        width: 75%;
    }

    #xp #right h3 {
        font-size: 20px;
    }

    .fw600 {
        font-weight: 600;
    }

    .mtb8 {
        margin: 8px 0px;
    }

    #date {
        font-style: italic;
        font-size: 14px;
    }

    .company {
        border-left: 4px solid var(--vt-c-custom-text-1);
        line-height: 30px;
        padding-left: 10px;
    }

    .active {
        border-left: 4px solid var(--vt-c-custom-text-2);
        color: var(--vt-c-custom-text-2);
    }

    .company:hover {
        cursor: pointer;
        color: var(--vt-c-custom-text-1);
    }

    .hide {
        display: none;
    }

    @media screen and (max-width: 600px) {
        #xp #right {
            width: 100%;
            margin-top: 20px;
        }
        #xp #left {
            width: 100%;
        }
        .company {
            border: none;
            padding-left: 0px;
            float: left;
            margin-right: 10px;
        }
    }
</style>