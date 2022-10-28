<template>
<h1 class="gd">good morning  {{fullname}}</h1>
<h2>your current count is {{count}}and the name is {{firstname}} {{lastname}}</h2>
<button v-on:click="increment()">click</button>
</template>
<script>
import {  computed, reactive ,ref,toRefs}  from 'vue';
export default {
    name:"HomeComp",
setup(){
const count = ref("0");
 const height = ref("100px")
const user = reactive({
    firstname:"akash patel",
    lastname:"ranjan",
    free:"yes"
})
function increment(){
    count.value++;
}
const fullname  = computed(()=>{
    return user.firstname +" " + user.lastname;
})
return{
    count,
    increment,
    ...toRefs(user),
    fullname,
    height
 }

}


}
</script>

<style scoped>
.gd{
    color:blue;
    background-color: beige;
    height:v-bind(height);
    width:v-bind(width);
    padding: 20px;
}
</style>