<template>
  <div class="about">
    <el-button type="primary" style="margin-left: 16px" @click="drawer = true">
    点击打开drawer
  </el-button>

  <el-drawer v-model="drawer">
    <template #header>
      <h4>set title by slot</h4>
    </template>
    <template #default>
      <div>
        <el-radio v-model="radio1" label="Option 1" size="large"
          >Option 1</el-radio
        >
        <el-radio v-model="radio1" label="Option 2" size="large"
          >Option 2</el-radio
        >
      </div>
    </template>
    <template #footer>
      <div style="flex: auto">
        <el-button @click="drawer = false">cancel</el-button>
        <el-button type="primary" >confirm</el-button>
      </div>
    </template>
  </el-drawer>
  </div>
</template>
<script>
export default{
    name: "ResultRecords",
    data() {
        return {
           drawer: false
        }
    },
  }
</script>