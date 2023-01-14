<template>
    <div class="skills-wrapper">
        <div v-for="skillsItem in resume.skills" :key="skillsItem.id" class="progress-wrapper px-3 d-flex flex-column w-100">
            <div class="progress-text justify-content-between d-flex text-capitalize">
                <p class="name">{{skillsItem.title}}</p>
                <p class="rating">{{skillsItem.rate}}%</p>
            </div>
            <div  class="progress progress-bar-progress" role="progressbar" :aria-valuenow="skillsItem.rate" aria-valuemin="0" aria-valuemax="100">
                <div class="progress-bar progress-bar-striped rounded-2" :style="{width: skillsItem.rate + '%'}"></div>
            </div>
        </div>
    </div>
    
</template>
<script>
import {mapActions, mapGetters} from 'vuex';
export default {
    name: 'SkillsItem',
    computed: {
        ...mapGetters(['resume']),
    },
    methods: {
        ...mapActions(['fetchResume']), 
    },
    created(){
        this.fetchResume();
    },
}
</script>
<style scoped>

    .progress-bar-progress {
        height: 10px;
        transform: translateY(-.5rem);
    }
    .progress-bar {
        background: var(--theme-color);
    }

    .skills-wrapper {
        overflow: auto;
        padding: 1.5rem;
        display: grid;
        grid-template-columns: repeat(2,1fr);
        grid-template-rows: 2fr repeat(5, 3fr);
    }

    @media screen and (max-width: 800px) {
        .skills-wrapper {
            display: flex;
            flex-direction: column;
        }
    }

    @media screen and (max-width: 500px) {
        .progress-wrapper {
            margin: 0;
            width: 120% !important;
            transform: translateX(-1rem);
        }
    }
</style>