<template>
  <div class="sider">
    <Menu theme="light" width="auto" @on-select="changePage">
      <Submenu name="1-1">
        <template slot="title">
         <Icon type="ios-apps" />
          多级菜单
        </template>
        <Submenu name="1-1-1">
          <template slot="title"> 
            <Icon type="ios-bus" />
            表格 </template>
          <MenuItem
            v-for="(item, index) in Data1"
            :key="index"
            :name="item.name"
            >{{ item.title }}</MenuItem
          >
        </Submenu>
        <Submenu name="1-1-2">
          <template slot="title">
          <Icon type="ios-clipboard" />
          图表
        </template>
        <MenuItem name="charts">Ecahrts实现</MenuItem>
        </Submenu>
      </Submenu>
    </Menu>
  </div>
</template>
<script>
export default {
  name: "Sider",
  data() {
    return {
      Data1: [
        {
          name: "table1", //此处的name用来路由跳转
          title: "表格",
        },
        {
          name: "table2",
          title: "表单",
        },
        {
          name: "table3",
          title: "其他",
        },
      ],
    };
  },
  methods: {
    changePage(name) {
      // console.log(name);
      this.$router.push(name);
    },
  },
};
</script>
<style scoped>
.sider {
  border: 1px solid #d7dde4;
  background-color: #fdfdfd;
  border-radius: 4px;
  overflow: hidden;
  width: 200px;
}
</style>