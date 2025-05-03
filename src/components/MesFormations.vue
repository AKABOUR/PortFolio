<script setup>
    
</script>

<template>
    <div id="tutos">
        <h2 class="text-highlight-1 section-title">Formations et certifications</h2>
        <div id="formations">
            <div class="formation">
                <span class="text-highlight-2"><h3>2007 – 2010 : ECOLE MAROCAINE DES SIENCES DE L’INGENIEUR (EMSI RABAT)</h3></span>
                <p>Diplôme d’ingénieur Génie Informatique & Réseaux, option Miage.</p>
            </div>
            <div class="formation">
                <span class="text-highlight-2"><h3>2009 : CERIFICATION MICROSOFT</h3></span> 
                <p>­315 Developing and Implementing Web Applications with Microsoft® Visual C#™ .NET and Microsoft® Visual Studio® .NET.</p>
            </div>
            <div class="formation">
                <span class="text-highlight-2"><h3>2008 : CERIFICATION MICROSOFT</h3></span>
                <p>­431 TS: Microsoft® SQL Server™ 2005 - Implémentation and Maintenance.</p>
            </div>
            <div class="formation">
                <span class="text-highlight-2"><h3>2004 – 2006 : ISTA HAY RIAD (RABAT)</h3></span>
                <p>Diplôme de technicien spécialisé en développement informatique.</p>
            </div>
            <div class="formation">
                <span class="text-highlight-2"><h3>2004 : BAC SCIENTIFIQUE</h3></span>
                <p>BAC Scientifique (Lycée Ibn Rochd RABAT).</p>
            </div>        
        </div>
    </div>
</template>

<style scoped>
    #tutos {
        margin-top: 60px;
    }
    #tutos .description {
        text-align: justify;
        font-size: 19px;
    }
    #formations {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        grid-template-rows: repeat(1, 1fr);
        grid-column-gap: 2px;
        grid-row-gap: 5px;
        margin-top: 1px;
    }
    .formation img {
        width: 100%;
    }
    .formation h3 {
        font-size: 20px;
        font-weight: bold;
    }
    .formation p {
        font-size: 17px;
        text-align: justify;
    }
    .formation a {
        color: white;
        text-decoration: underline;
        text-underline-offset: 4px;
    }
    #formateur {
        line-height: 40px;
        color: white;
        text-decoration: underline;
        text-underline-offset: 4px;
        font-size: 20px;
        font-weight: bold;
        display: block;
        width: 100%;
        text-align: center;
        margin-top: 40px;
    }

    @media screen and (max-width: 600px) {
        #formations {
            grid-template-columns: repeat(1, 1fr);
            grid-template-rows: repeat(1, 1fr);
            grid-column-gap: 0px;
            grid-row-gap: 20px;
        }
    }
</style>