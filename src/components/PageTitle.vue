<script setup>
    import SocialIcon from './SocialIcon.vue';
</script>

<template>
    <div id="top-line">
        <img id="profile-img" src="../assets/me.jpeg" alt="me" width="300px" height="300px" />
        <div id="line">
            <p>Je suis <span class="text-highlight-1">Said AKABOUR</span>, <br/>
                Développeur Fullstack .Net / MERN</p>
            <div id="social">
                <SocialIcon img="linkedin" alt="linkedin" link="https://www.linkedin.com/in/said-akabour/" />
                <SocialIcon img="github" alt="github" link="https://github.com/AKABOUR/" />
                <SocialIcon img="facebook" alt="facebook" link="https://fr-fr.facebook.com/public/Said-Akabour" />
            </div>
        </div>
    </div>
</template>

<style scoped>
img {
border-radius: 50%;
border: 5px solid #ababf8;
}
    #top-line {
        margin-top: 10px;
        width: 100%;
        height: 300px;
    }

    #top-line #profile-img {
        float: left;
        margin-right: 50px;
    }

    #top-line #line {
        float: left;
        transform: translateY(40%);
        text-align: center;
    }

    #top-line p {
        font-size: 42px;
        line-height: 60px;
    }

    #top-line p span {
        font-weight: bold;
    }

    #social {
        margin-top: 15px;
    }

    @media screen and (max-width: 905px) {
        #top-line #profile-img {
            display: none;
        }

        #top-line #line {
            float: none;
            transform: translateY(0%);
        }

        #top-line p {
            font-size: 36px;
        }
    }
</style>