<template>
    <div 
        :class='isAlive.isAlive ? "alive":"dead"'
        class='cell'
    >
    </div>
</template>
<script>
export default {
    name: 'Cell',
    props: {
        statusObj: {
            default: function() {
                return { isAlive: false };
            },
            type: Object,
        },
        xPos: {
            default: -1,
            type: Number,
        },
        yPos: {
            default: -1,
            type: Number,
        }
    },
    data() {
        return {
            isAlive: this.statusObj
        }
    }
}
</script>
<style scoped>
.cell {
    border-right: 1px dotted black;
    border-bottom: 1px dotted black;
    height: 5px;
    width: 5px;
}
.cell:hover {
    background-color: #0099ff;
}
.alive {
    background-color: #0004ff;
}
</style>