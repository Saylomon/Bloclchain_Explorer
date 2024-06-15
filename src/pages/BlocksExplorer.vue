<template>
    <div>
        <block 
            v-for:='block in $store.state.blocks'
            :block="block"
        />
    </div>
</template>

<script>
import {mapActions} from 'vuex'
export default {
    name: "BlocksExplorer",
    methods: {
        ...mapActions({
            newBlockHeaders: "newBlockHeaders",
        })
    },
    async mounted() {
        this.newBlockHeaders()
    },
}
</script>


<style>
.info{
    border: 2px solid purple;
    padding: 1px 3px;
}
button{
    padding: 7px;
    margin: 5px;
    margin-top: 2px;
    border: 2px solid purple;
    margin-bottom: 10px;
    color: purple;
}
.block_info{
    border: 7px solid rgb(124, 6, 110);
    margin: 50px;
    padding: 10px; 
    font-family: 'Times New Roman', Times, serif;
    margin-top: 35px;
}
input{
    border: 2px solid purple;
    margin: 5px;
    padding: 7px;
}
.title{
    margin: 5px;
    padding: 5px 5px;
    border: 2px solid purple;
    font-family: Arial, Helvetica, sans-serif;
    /* font-size: auto; */
    display: flex;
    justify-content: center;
    width: auto;
    height: auto;
    align-self: center;
    text-align: center;
}
</style>