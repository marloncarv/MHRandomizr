<template>
    <v-col>
        <div class="subtitle">
            Weapon
        </div>
        <div class="monster-name">
            {{selectedWeapon}}
        </div>
    </v-col>
</template>

<script>
import WEAPONLIST from './weaponsList.js'

export default {
    data(){
        return {
            selectedWeapon: null
        }
    },

    methods: {
        getRandomWeapon() {
            const min = Math.ceil(0)
            const max = Math.floor(WEAPONLIST.length - 1)
            this.selectedWeapon = WEAPONLIST[Math.floor(Math.random() * (max - min + 1)) + min]
        }
    }
}
</script>