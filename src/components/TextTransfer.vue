<template>
  <div>
    <div class="connect_btn">
      <button id="openBroadcast" @click="btn_open_broadcast">打开广播</button>
      <button id="closeBroadcast" @click="btn_close_broadcast">关闭广播</button>
    </div>
    <div class="user_list">
      <button id="test_user" @click="user_click">测试用户1</button>
    </div>
    <div>
      <input id="send_text" :value="sendContent" />
      <button id="send_btn" @click="btn_send">发送</button>
    </div>
    <div>
      <input id="accept_text" :value="acceptContent" />
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Options } from "vue-class-component";

@Options({
  props: {},
})
export default class TextTransfer extends Vue {
  public sendContent = "";
  public acceptContent = "";

  mounted() {
    this.sendContent = "这是发送的内容";
    this.acceptContent = "这是接收的内容";
  }

  /**
   * btn_open_broadcast
   * 打开连接
   */
  public btn_open_broadcast(): void {
    console.log("open broadcast");
  }
  /**
   * btn_close_broadcast
   * 关闭连接
   */
  public btn_close_broadcast(): void {
    console.log("close broadcast");
  }

  /**
   * user_click
   * 点击用户头像
   */
  public user_click() {
    console.log("click user to connect");
  }

  /**
   * btn_send
   * 发送文本到另一端
   */
  public btn_send() {
    this.sendContent = "我发送了一条信息";
    this.acceptContent = "我接收了一条消息";
  }
}
</script>

<style>
.connect_btn {
  margin-top: 1%;
  margin-bottom: 1%;
}
.user_list {
  margin-top: 1%;
  margin-bottom: 1%;
  background: cadetblue;
}
#send_text {
  margin-top: 1%;
  margin-bottom: 1%;
  width: 90%;
}
#send_btn {
  width: 10%;
}
#accept_text {
  margin-top: 1%;
  margin-bottom: 1%;
  resize: none;
  width: 90%;
}
</style>
