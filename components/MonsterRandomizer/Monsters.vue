<template>
    <v-col>
        <div class="subtitle">
            Monster
        </div>
        <div class="monster-name">
            {{selectedMonster}}
        </div>
    </v-col>
</template>

<script>
import MONSTERLIST from './monstersList.js'

export default {
    data(){
        return {
            selectedMonster: null
        }
    },

    methods: {
        getRandomMonster() {
            const min = Math.ceil(0)
            const max = Math.floor(MONSTERLIST.length - 1)
            this.selectedMonster = MONSTERLIST[Math.floor(Math.random() * (max - min + 1)) + min]
        }
    }
}
</script>

