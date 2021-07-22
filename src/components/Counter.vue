<template>
    <div class="mb-20">
      Counter: {{ number }}
      <div>
          <label for="counter" :title="number">Counter: </label>
          <input type="text" v-model="number"/>
            <button @click="decrease">-</button>
            <button v-on:click="increase(10)">+</button>
            <button v-on:click="addTen">+10</button>
      </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            number: this.initNumber || 10,
        }
    },
    props: ['initNumber'],
    methods:{
        increase(number){
            this.number+=number;
        },
        addTen(){
            this.number+=10;
        },
        decrease(){
            this.number--;
        }
    }
}
</script>

<style lang="scss" scoped> 
.mb-20{
    margin-bottom: 20px;
}
</style>