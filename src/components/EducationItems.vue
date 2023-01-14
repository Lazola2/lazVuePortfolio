<template>
    <div class="edu-wrapper w-100">
        <div v-for="item in resume.education" :key="item" class="item item-1 p-0 m-0">
            <h4 class="item-title d-flex gap-md-2">
                <i :class="item.iconClassName"></i>
                {{ item.name }}
            </h4>
            <div class="item-paragraph ps-5 mt-1">
                <li v-for="title in item.modules" :key="title" class="title">
                    {{ title }}
                </li>
            </div>
        </div>
    </div>
    
</template>
<script>
import {mapActions, mapGetters} from 'vuex';
export default {
    name: 'EducationItems',
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
.item {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
}
.item-title {
    scale: .8;
    position:relative;
}
.icon {
    scale: 1.7;
}

.brush, .code-icon {
    font-size: 35px;
}
.item-title::before {
    content: '';
    width: 2.5rem;
    height: 2.5rem;
    background: var(--theme-color);
    border-radius: 50%;
    position: absolute;
    z-index: -1;
    left: -1rem;
    top: -.5rem;
}

.item-paragraph {
    text-align: left;
    font-size: 14px;
    width: 90%;
}

.edu-wrapper {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1.5fr repeat(2, 5fr);
}

@media screen and (max-width: 800px) {  
    .edu-wrapper {
        display: flex;
        flex-direction: column;
        gap: 2.5rem;
        padding: 1rem 0 2rem 1.5rem;
        overflow-y: auto;
    }

    .title {
        font-size: 15px;
    }
}

@media screen and (max-width: 500px) {
    
    .item-title {
        width: 100%;
        transform: translateX(-1rem);
        text-align: left;
    }

    .item-title::before {
        display: none;
    }

    i {
        display: none;
    }

    li {
       
        width: 166%;
        translate: -2.3rem -.5rem;
        font-size: 14px !important;
    }
}



</style>