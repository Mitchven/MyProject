<template>
  <sidebar-menu :menu="menu" style = "margin-top: 56px;height:93%"/>
</template>

<style scoped>
 
</style>
 
<script>
export default {
  data() {
    return {
      menu: [
        {
          header: true,
          title: "Main Navigation",
          hiddenOnCollapse: true
        },
        {
          href: "/Dashboard",
          title: "Dashboard",
          icon: "fa fa-chart-area",
        },
        {
          href: "/Subjects",
          title: "Subjects",
          icon: "fa fa-chart-area",
        },
        {
          href: "/PersonalInfo",
          title: "Personal Info",
          icon: "fa fa-chart-area",
        },
        {
          href: "/Login",
          title: "Logout",
          icon: "fa fa-chart-area",
        }
      ]
    };
  }
};
</script> 