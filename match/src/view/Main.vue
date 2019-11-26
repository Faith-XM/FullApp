<template>
  <div class="main h-100 w-100 bg-primary-2">
    <div class="content">
      <div class="top bg-white d-flex flex-column">
        <div class="logo">
          <img src="../assets/img/LOGO@2x(1).png" alt />
        </div>
        <ul class="mao">
          <li class="listBug">
            <a :class="{active:shows==1}" @click="main()">首页</a>
            <a :class="{active:shows==2}" @click="about()">关于我们</a>
            <a :class="{active:shows==3}" @click="classes()">火柴课堂</a>
            <a :class="{active:shows==4}" @click="teacher()">师资力量</a>
            <a :class="{active:shows==5}" @click="category()">班级类别</a>
          </li>
        </ul>
        <div id="marker"></div>
      </div>
      <!-- <div id="abb">
        <div class="abb">
          cdsvdsv vgfd gdf
        </div>
      </div> -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      shows: 1
    };
  },
  methods: {
    main() {
      this.shows = 1;
    },
    about() {
      this.shows = 2;
    },
    classes() {
      this.shows = 3;
    },
    teacher() {
      this.shows = 4;
    },
    category() {
      this.shows = 5;
    }
  }
};
</script>

<style scoped>
.mao {
  display: flex;
  flex-direction: row;
  margin-left: 186.9994px;
  font-size: 14px;
  width: 50rem;
  justify-content: space-between;
  border-bottom: 0.2143rem solid transparent;
  color: #333;
}
/* .miao {
  color: #f47a2d;
  border-bottom: 3px solid #f47a2d;
} */
a:hover {
  color: #f47a2d;
  border-bottom: 3px solid #f47a2d;
}
.active {
  color: #f47a2d;
  border-bottom: 3px solid #f47a2d;
}
.content{
  width: 71.4286rem;
  height: 100%;
  background-color: antiquewhite;
  margin: 0 auto;
}
.listBug{
  height: 100rem;
  background-color: #f47a2d
}
/* #abb{
  width: 137.1429rem;
  height: 100%;
  background-color: #f47a2d;
} */
</style>