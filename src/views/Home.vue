<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import{
  createApp,//创建一共App实例
  onMounted,//跟之前的mounted一样 只是写法不一样
  computed,//写法变了
  watch,//写法变了
  watchEffect,//新增的watchEffect 立即执行传入的一个函数，并响应追踪其以来 在其依赖改变时 重新运行
  reactive,//传入一个普通对象返回一个响应对象
  ref,    //接受一个参数值并返回一个响应式且可改变的ref对象 ref对象拥有一个指向内部值的单一属性 。value
  toRef,  //可以用来为一个reactive 对象的属性创建一个 ref
  toRefs,  //把一个响应式对象转换为普通对象 转化后可以使用 。。。解构出来2
  nextTick
 } from 'vue'
import { Options, Vue, } from 'vue-class-component';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Options({
  components: {
    HelloWorld,
  },
})
export default class Home extends Vue {}
</script>
