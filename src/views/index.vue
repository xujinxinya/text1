<template>
  <div class="dahezi">
    <div class="logo">
      <div class="tu">
        <img src="../assets/img/logo.png" alt="#" width="82px" height="125px" />
      </div>
    </div>
    <div class="main">
      <div class="name">大宝贝助手</div>

      <div class="text">{{ tt }}</div>

      <div class="btn">
        <label for="file" class="btn">
          <p class="zi">选择文件</p>
        </label>
      </div>
      <input
        type="file"
        id="file"
        name="file"
        class="cc"
        ref="file"
        multiple="multiple"
        @change="get($event)"
      />

      <button class="shangchuan" @click="aa">上传文件</button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      tt: "选择要上传的文件",
      files: [],
    };
  },

  methods: {
    get(e) {
      var fo = document.getElementById("file").files[0];
      this.tt = fo.name;
      console.log(e);
    },
  },
};
</script>
<style>
.dahezi {
  width: 293px;
  height: 516px;
  background-color: #303030;
  margin: auto;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  display: flex;
  flex-direction: column;
  border-radius: 10px;
}

.logo {
  width: 293px;
  height: 232px;
}

.tu {
  text-align: center;
  line-height: 232px;
}

.main {
  width: 293px;
  height: 284px;
  background-color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  position: relative;
}

.name {
  margin-top: 25px;
  height: 14px;
  font-size: 14px;
  font-weight: 550;
  color: #485963;
}

.text {
  margin-top: 28px;
  color: #5db8d9;
  font-size: 12px;
  font-weight: 550;
}

.zi {
  text-align: center;
  line-height: 41px;
  color: white;
  cursor: default;
}

.btn:hover {
  background-color: #428fd3;
}

.btn:active {
  top: 2px;
}

.cc {
  margin-top: 65px;
  width: 150px;
  height: 41px;
  position: absolute;
  opacity: 0;
}

.btn {
  position: relative;
  width: 150px;
  height: 41px;
  background-color: #60a9c1;
  margin-top: 28px;
  border-radius: 15px;
}

.shangchuan {
  width: 150px;
  height: 41px;
  background-color: #5ac189;
  text-align: center;
  line-height: 41px;
  margin-top: 5px;
  border-radius: 15px;
  color: white;
  cursor: default;
  position: relative;
}

.shangchuan:hover {
  background-color: rgb(22, 145, 69);
}

.shangchuan:active {
  top: 2px;
}
</style>
