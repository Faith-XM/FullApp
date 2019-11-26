<template>
  <div class="about">
    <p>Original message: "{{ message }}"</p>
    <p>Computed reversed message: "{{ reversedMessage }}"</p>
    <ul >
      <li 
      v-on:mouseover="changeActive($event)" 
      v-on:mouseout="removeActive($event)"
      v-for="(item, i) in heroes " 
      :key="i"
      >{{item.name}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      message: "Hello",
      heroes: [
        {
          name: "孙悟空",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/167/167.jpg"
        },
        {
          name: "鲁班七号",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/112/112.jpg"
        },
        {
          name: "铠",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/193/193.jpg"
        },
        {
          name: "后羿",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/169/169.jpg"
        },
        {
          name: "亚瑟",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/166/166.jpg"
        },
        {
          name: "孙尚香",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/111/111.jpg"
        },
        {
          name: "安琪拉",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/142/142.jpg"
        },
        {
          name: "甄姬",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/127/127.jpg"
        },
        {
          name: "妲己",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/109/109.jpg"
        },
        {
          name: "韩信",
          avater:
            "https://game.gtimg.cn/images/yxzj/img201606/heroimg/150/150.jpg"
        }
      ],
      currentIndex:0,
    };
  },
  computed: {
    // 计算属性的 getter
    reversedMessage: function() {
      // `this` 指向 vm 实例
      return this.message
        .split("")
        .reverse()
        .join("");
    },
    pvp() {
      this.heroes.map((item, i) => {});
      return item;
    }
  },
  methods: {
    // 鼠标移入加入class
    changeActive($event) {
      $event.currentTarget.className = "active";
    },
    removeActive($event) {
      $event.currentTarget.className = "";
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul{
  width: 71.4286rem;
  /* height: ; */
  background-color: aliceblue;
  display: flex;
  flex-direction: row;
}
li{
  flex: 1;
}
.active{
  color: red;
  border-bottom: 1px solid black; 
}
</style>
