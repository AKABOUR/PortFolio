<script setup>

</script>

<template>
    <div id="skills">
        <h2 class="text-highlight-1 section-title">Domaines de compétences</h2>
        <div id="icons-list">
            <div class="techno-container"><i class="techno-icon devicon-csharp-plain"></i> <br/> <span>CSharp</span></div>
            <div class="techno-container"><i class="techno-icon devicon-dotnetcore-plain"></i> <br/> <span>DotNetCore</span></div>
            <div class="techno-container"><i class="techno-icon devicon-jira-plain"></i> <br/> <span>JIRA</span></div>
            <div class="techno-container"><i class="techno-icon devicon-android-plain"></i> <br/> <span>Android</span></div>
            <div class="techno-container"><i class="techno-icon devicon-html5-plain"></i> <br/> <span>HTML</span></div>
            <div class="techno-container"><i class="techno-icon devicon-css3-plain"></i> <br/> <span>CSS</span></div>
            <div class="techno-container"><i class="techno-icon devicon-javascript-plain"></i> <br/> <span>JS</span></div>
            <div class="techno-container"><i class="techno-icon devicon-microsoftsqlserver-plain"></i> <br/> <span>SQL</span></div>
            <div class="techno-container"><i class="techno-icon devicon-mysql-original"></i> <br/> <span>MySQL</span></div>   
            <div class="techno-container"><i class="techno-icon devicon-sqlite-plain"></i> <br/> <span>SQLLite</span></div>
            <div class="techno-container"><i class="techno-icon devicon-postgresql-plain"></i> <br/> <span>PostgreSQL</span></div>
            <div class="techno-container"><i class="techno-icon devicon-git-plain"></i> <br/> <span>Git</span></div>
            <div class="techno-container"><i class="techno-icon devicon-docker-plain"></i> <br/> <span>DOCKER</span></div>
            <div class="techno-container"><i class="techno-icon devicon-graphql-plain"></i> <br/> <span>GraphQL</span></div>
            <div class="techno-container"><i class="techno-icon devicon-prisma-plain"></i> <br/> <span>Prisma</span></div>
            <div class="techno-container"><i class="techno-icon devicon-bootstrap-plain"></i> <br/> <span>Bootstrap</span></div>
            <div class="techno-container"><i class="techno-icon devicon-react-original"></i> <br/> <span>React</span></div>
            <div class="techno-container"><i class="techno-icon devicon-jquery-plain"></i> <br/> <span>jQuery</span></div>
            <div class="techno-container"><i class="techno-icon devicon-vuejs-plain"></i> <br/> <span>VueJS</span></div>
            <div class="techno-container"><i class="techno-icon devicon-vuetify-plain"></i> <br/> <span>Vuetify</span></div>
            <div class="techno-container"><i class="techno-icon devicon-angularjs-plain"></i> <br/> <span>AngularJS</span></div>
            <div class="techno-container"><i class="techno-icon devicon-vite-original"></i> <br/> <span>Vite</span></div>
            <div class="techno-container"><i class="techno-icon devicon-postman-plain"></i> <br/> <span>POSTMAN</span></div>
        </div>
    </div>
</template>

<style scoped>
    #skills {
        margin-top: 60px;
    }

    #icons-list {
        display: grid;
        grid-template-columns: repeat(8, 1fr);
        grid-template-rows: repeat(2, 1fr);
        grid-column-gap: 5px;
        grid-row-gap: 50px;
        margin-top: 35px;
    }

    .techno-container {
        text-align: center;
        color: var(--vt-c-custom-text-1); 
        transition: transform 0.5s;
    }

    .techno-container span {
        font-weight: bold;
    }

    .techno-container:hover {
        transform: rotate(15deg);
        color: var(--vt-c-custom-text-2);
    }

    .techno-icon {
        font-size: 80px;
        margin: 0 auto;
        color: var(--vt-c-custom-text-1);
    }

    .techno-icon:hover {
        color: var(--vt-c-custom-text-2);
        transform: rotate(15deg);
    }

    @media screen and (max-width: 905px) {
        #icons-list {
            grid-template-columns: repeat(4, 1fr);
            grid-template-rows: repeat(4, 1fr);
            grid-column-gap: 5px;
            grid-row-gap: 40px;
        }
    }

    @media screen and (max-width: 450px) {
        #icons-list {
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(8, 1fr);
            grid-column-gap: 5px;
            grid-row-gap: 20px;
        }
    }
</style>