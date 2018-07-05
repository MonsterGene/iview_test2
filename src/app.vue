<template>
    <div id="app">
        <!-- <div id="cover"></div>  -->
        <Form :model="formModel" inline>
            <FormItem label="List :" :label-width="100">
                <Select v-model="formModel.list">
                    <Option
                        v-for="item in list"
                        :key="item"
                        :value="item"
                        v-text="item"
                    ></Option>
                </Select>
            </FormItem>
        </Form>
        <!-- <Header></Header>
        <todo></todo>
        <Footer></Footer> -->
    </div>
</template>
<script>
import {Form,FormItem,Select,Option} from "iview"
export default {
   components:{
       Form,
       FormItem,
       Select,
       Option
   },
   data:function(){
        return {formModel:{
            list:[
                "item 1",
                "item 2",
                "item 3",
                "item 4"
            ]
        }}
   }
}
</script>
<style lang="stylus" scoped>
#app{
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
}
#cover{
    position: absolute;
    left: 0
    top:0
    right 0
    bottom 0
    background-color #999
    opacity .9
    z-index: -1
}
</style>
