<script setup>
import { computed, watch } from 'vue';

const zxse = ref(0)
const xse = ref(0)
const xsrw = ref(0)
const wcl = ref(0)
const dbkf = ref(0)
watch([xse,xsrw],([x,y])=>{
    const va = x/y*100
    if(va>100){
        wcl.value = 100
    }
    else if(0<=va<=100){
        wcl.value = va
    }else{
        wcl.value = 100
    }
})
</script>
<template>
    <div class="container mx-auto h-screen *:m-2 scale-75 md:scale-100">
        <h1 class="text-center text-3xl">提成计算</h1>
        <div>
            <label for="" class=" inline-block w-32 ">月总销售额</label>
            <input type="number" v-model="zxse" class="input input-bordered">
        </div>
        <div>
            <label for="" class=" inline-block w-32 ">个人销售额</label>
            <input type="number" v-model="xse" class="input input-bordered">
        </div>
        <div>
            <label for="" class=" inline-block w-32 ">销售额任务</label>
            <input type="number" v-model="xsrw" class="input input-bordered"> <span>完成率：{{ (wcl>100? 100: wcl).toFixed(2) }}%</span>
        </div>
        <div>
            <label for="" class=" inline-block w-32 ">代班客服</label>
            <input type="number" v-model="dbkf" class="input input-bordered">
        </div>
        <div class="bg-slate-200 rounded-lg *:p-4">
            <p class="my-4 p-4 ">提成计算公式：</p>
            <p>个人销售额 <span class="kbd">{{ xse }}</span> X 5%  =  <span class="kbd">{{ xse * 0.05 }}</span></p>
            <p>团队提成 <span class="kbd">{{ zxse }}</span> X 1% X 完成例 {{ wcl.toFixed(2) }}%  =  <span class="kbd">{{ (zxse * 0.01*wcl/100).toFixed(2)  }} </span>  </p>
            <p>代班客服提成 <span class="kbd">{{ dbkf }}</span> X 1%  =  <span class="kbd ">{{ dbkf * 0.01 }}</span></p>
            <p>提成合计： <span class="kbd ">{{ xse * 0.05 }}</span> + <span class="kbd">{{ (zxse * 0.01*wcl/100).toFixed(2)  }} </span> + <span class="kbd">{{ dbkf * 0.01 }}</span> = 
                <span class="kbd">{{ ((xse * 0.05) + (zxse * 0.01*wcl/100) + (dbkf * 0.01)).toFixed(2) }}</span></p>
        </div>
    </div>
</template>