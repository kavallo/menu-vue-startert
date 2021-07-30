<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <!-- <HelloWorld msg="Hello Vue 3 + Vite" /> -->
  <sidebar-menu
    :menu="menu"
    update:collapsed="onToggleCollapse"
    @item-click="onItemClick"
  />
</template>
<script>
export default {
  data() {
    return {
      menu: [
        {
          header: "Main Navigation",
          hiddenOnCollapse: true,
        },
        {
          href: "/",
          title: "Dashboard",
          icon: "fa fa-user",
        },
        {
          href: "/charts",
          title: "Charts",
          icon: "fa fa-chart-area",
          child: [
            {
              href: "/charts/sublink",
              title: "Sub Link",
            },
          ],
        },
      ],
    };
  },
  methods: {
    onToggleCollapse(collapsed) {
      alert(0);
      alert(collapsed);
    },
    onItemClick(event, item) {
      alert(1);
      alert(event);
      alert(item);

      console.log(event);
      console.log(item);
    },
  },
};
</script>