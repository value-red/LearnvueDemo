<template>
  <div id="list">
    <table class="table table-border table-hover table-striped">
      <thead>
      <tr>
        <th>ID</th>
        <th>Name</th>
        <th>Time</th>
        <th>Option</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="item in list" :key="item.id">
        <td>{{item.id}}</td>
        <td v-text="item.name"></td>
        <td>{{item.time}}</td>
        <td>{{item.option}}</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
  export default {
    name: "list"
  }
  new Vue({
    el: "#list",
    data: {
      list: [
        {id: 1, name: "宝马", time: '', option: "删除"},
        {id: 2, name: "悍马", time: '', option: "删除"}
      ]
    }
  })
</script>

<style scoped>

</style>
