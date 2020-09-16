<template>
  <div id="contain">
    <div id="input" style="padding: 2px;">
      <el-input
      v-model="input"
      placeholder="请输入待办事项"
      @keyup.enter="add"
      style="width: 100%;"
      >       
      </el-input>
    </div>
    <div id="to-do-list">
      <div id="item" 
      v-for="todo in todos"
      :key="todo.index"
      >     
        <ToDoItem>          
        </ToDoItem>
      </div>
      <div id="footer">
        <div id="leftNum">

        </div>
        <div id="clear">
          <el-button>

          </el-button>
        </div>
      </div>
    </div>

  </div>
  
</template>

<script>
  export default{
    data(){
      return{
        input:'',
        todos:[
          {index:1,item:"待办事项"}
        ]
      }
    },
    methods:{
      add(){

      }
    }
  }
</script>

<style>
  #contain{
    width: 35%;
    border: 2px solid lightblue; 
    text-align: center;
    margin:0 auto;
  }
  #to-do-list{
    width:auto;
    border: 2px solid lightblue;
    padding: 2px;
  }
</style>