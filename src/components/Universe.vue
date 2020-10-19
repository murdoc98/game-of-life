<template>
    <div class="universe">
        <div
            v-for='(col, indexX) in universe'
            :key='indexX'
            class="universe-column"
        >
            <Cell
                v-for='(isAlive, indexY) in col'
                :key='indexY'
                :status-obj='isAlive'
                :x-pos='indexX'
                :y-pos='indexY'
            />
        </div>
    </div>
</template>
<script>
import Cell from './Cell.vue';
export default {
    name: 'Universe',
    components: {
        Cell
    },
    data() {
        return {
            x: 250,
            y: 100,
            universe: []
        }
    },
    created() {
        this.generateUniverse();
    },
    methods: {
        generateUniverse: function() {
            for(let i = 0; i < this.x; i++) {
                this.universe[i] = [];
                for(let j = 0; j < this.y; j++) {
                    this.universe[i][j] = { isAlive:false };
                }
            }
        }
    }
}
</script>
<style scoped>
.universe {
    border: 2px solid #3700ce;
    width: max-content;
    margin: 0 auto;
    border-radius: 2px;
    display: flex;
    justify-content: center;
}
.universe-column {
    display: flex;
    justify-content: center;
    padding: 0;
    margin: 0;
    flex-direction: column;
}
</style>