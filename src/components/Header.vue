<template>
  <div id="TalionNav">
    <header class="TalionNav">
      <div class="TalionNav-primary">
        <nav>
          <ul>
            <li><a href="#/movies" style="color: #fff">三千越甲</a></li>
          </ul>
          <span class="search"></span>
        </nav>
      </div>
    </header>
    <slot></slot>
    <footer class="footer">
      <hr />
      <div class="footer_bottom">
        <div class="footer_left">
          <ul>
            <li>
              <a href="">关于</a>
            </li>
            <li>
              <a href="">开发计划</a>
            </li>
            <li>
              <a href="">特别鸣谢</a>
            </li>
          </ul>
        </div>
        <div class="footer_right">
          <span>
            ICP备案:<a
              href="https://beian.miit.gov.cn"
              target="_blank"
              rel="noopener noreferrer"
            >
              京ICP备2021000175号</a
            >
          </span>
          <br />
          <span>©2021 uponup.cn</span>
        </div>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      query: "",
      placeholder: "",
      path: "search-movie",
    };
  },
  mounted() {
    if (this.$route.path === "index" || this.$route.path.indexOf("movie")) {
      this.path = "/movie/search";
    } else if (this.$route.path.indexOf("book")) {
      this.path = "/book/search";
    }
  },
  methods: {
    search() {
      this.$router.push({ path: this.path, query: { query: this.query } });
      this.query = "";
    },
  },
};
</script>
<style>
#TalionNav {
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  z-index: 9999;
  background: #fff;
}

.TalionNav-primary {
  border-bottom: 1px solid #f3f3f3;
  -webkit-box-pack: justify;
  justify-content: space-between;
  -webkit-box-align: center;
  align-items: center;
  padding: 0px 42px;
  background: #fff;
  height: 60px;
  box-sizing: border-box;
  display: -webkit-box;
  display: flex;
  background: #383735;
}

nav li {
  display: inline-block;
}

nav li {
  font-size: 18px;
  margin-right: 29px;
}

ul,
li {
  margin: 0;
  padding: 0;
  list-style: none;
}

a {
  text-decoration: none;
}

.footer {
  position: fixed;
  bottom: 0;
  right: 0;
  left: 0;
  background-color: #383735;
  height: 134px;
  font-size: 14px;
  line-height: 1.2em;
  color: #fff;
  display: flex;
  flex-direction: column;
  text-align: center;
}

hr {
  display: block;
  width: 80%;
  border: 0;
  margin-top: 44px;
  border-top: 2px solid #727071;
  unicode-bidi: -moz-isolate;
}

.footer_bottom {
  width: 80%;
  line-height: 30px;
  margin-top: 30px;
  display: flex;
  flex-direction: row;
  margin-left: 10%;
  justify-content: space-between;
  line-height: 100%;
}

.footer_right a {
  background-color: transparent;
  color: #fff;
  transition: all 0.3s linear;
}

.footer_right {
  text-align: right;
  font-size: 12px;
  line-height: 20px;
  margin-top: -14px;
}

.footer_left {
}
.footer_left ul {
  display: flex;
  flex-direction: row;
  font-size: 15px;
}
.footer_left li {
  margin-right: 46px;
  display: inline-block;
  text-decoration: none;
}

.footer_left a {
  color: #fff;
  font-size: 19px;
}
</style>
