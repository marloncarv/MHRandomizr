<template>
    <v-container>
        <h1 class="main-title">
            MH Randomizr
        </h1>
        <v-row>
            <weapons ref="weapon-component" />
            <monsters ref="monster-component" />
        </v-row>
        <v-row>
            <v-col>
                <v-btn
                elevation="2"
                outlined
                @click="randomize"
                >
                Randomize!
                </v-btn>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import weapons from '../components/WeaponRandomizer/Weapons.vue'
import monsters from '../components/MonsterRandomizer/Monsters.vue'
export default {
    components: {
        weapons,
        monsters
    },

    methods: {
        randomize() {
            this.$refs['weapon-component'].getRandomWeapon()
            this.$refs['monster-component'].getRandomMonster()
        }
    }
}
</script> 