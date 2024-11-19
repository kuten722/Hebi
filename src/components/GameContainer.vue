<template>
  <div>
    <!-- 主容器 -->
    <div id="main">
      <!-- 游戏窗口 -->
      <GameStage></GameStage>
      <!-- 计分板 -->
      <GameScoreBoard></GameScoreBoard>
      <!-- 控制面板 -->
      <GameControlPanel></GameControlPanel>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import GameStage from './GameBox/GameStage.vue';
import GameScoreBoard from './GameBox/GameScoreBoard.vue';
import GameControlPanel from './GameBox/GameControlPanel.vue';

export default defineComponent({
  name: 'GameBox',
  components: {GameStage,GameScoreBoard,GameControlPanel}
});
</script>

<style lang="less">
  // 预设
  *{
    margin: 0;
    padding: 0;
    // 改变盒子的计算方式
    box-sizing: border-box;
  }
  body{
    font:bold 20px "Courier";
  }
  // 主容器
  #main {
    width: 360px;
    height: 450px;
    background-color: #FFFFFF;
    margin: 36px auto;
    border: 10px solid aqua;
    box-shadow: 0 0 15px rgb(0,0,0,50%);
    border-radius:20px;
    // 对齐
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-content:space-around;
  }
</style>
