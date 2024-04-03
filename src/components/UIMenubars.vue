<template>
  <div>
    <h2>UI Menubar Components</h2>
    <!-- Add your sidebars here -->
    <sidebar-menu :menu="menu" />
  </div>
</template>

<script>
import { SidebarMenu } from "vue-sidebar-menu";
import "vue-sidebar-menu/dist/vue-sidebar-menu.css";

export default {
  /*
  props: {

  }
  */
  components: {
    SidebarMenu,
  },
  data() {
    return {
      menu: [
        {
          header: "CDH",
          hiddenOnCollapse: false,
        },
        {
          href: "/home",
          title: "Home",
          icon: "pi pi-home",
        },
        {
          route: "/contact",
          title: "Contact",
          icon: "pi pi-address-book",
          child: [
            {
              href: "/contact/division1",
              title: "Division 1",
            },
            {
              href: "/contact/division2",
              title: "Division 2",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Add your styles here */
.v-sidebar-menu {
  /* can be changed to website theme vars later */
  --vsm-primary-color: #4285f4;
  --vsm-base-bg: #2a2a2e;
}
</style>
