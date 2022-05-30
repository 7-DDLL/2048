<template>
  
    <div class="news">

      <h4 style="letter-spacing: 8px;font-size: medium;padding: 1px;border: 1px;background: #b9b1aa;color: white;">新闻资讯</h4>

      <div class="news_ins">
        <img src="../assets/img/2.webp" style="width:88px;">
        <br>
        <br>
        <a class="bt" href="https://baijiahao.baidu.com/s?id=1670248450734965001&wfr=spider&for=pc">你玩《2048》能拿多少分？</a>
        <h5 >AI的最高分纪录：401912</h5>
        <pre>
如果让AI来玩《2048》这样的游戏，那会是怎样一种画面？

现在，有人用强化学习方法实践了起来。

于是，插上DQN的翅膀，AI从零起步，自己琢磨出了...
        </pre>
      </div>

      <div class="mdui-divider"></div>

      <!-- <div class="mdui-divider-inset"></div> -->

      <br>

      <div class="news_ins">
        <img class="right" src="../assets/img/4.webp" style="width:88px;">
        <br>
        <br>
        <a class="bt" href="https://baijiahao.baidu.com/s?id=1690212516550881228&wfr=spider&for=pc">《合成大西瓜》</a>
        <h5>2048+俄罗斯方块+水果忍者</h5>
        <pre>
  最近，小游戏《合成大西瓜》成为新晋流量爆款，在一众

明星八卦中杀出重围，吸引了瓜田里无数奔走的猹。针对

这一游戏的讨论也从微博知乎一直蔓延到豆瓣小红书...
        </pre>
      </div>
      <br>
      <br>
      
    </div>
 
</template>


<script>
// @ is an alias to /src

import 'mdui/dist/css/mdui.css';

export default{

}

</script>

<style scoped>

.news{
    /* font-size: large; */
    /* background: pink; */
    text-align: center;
}

.bt{
  /* font-size: larger; */
  font-weight:900;
  font-size: medium;
  color: #776e65;
  text-decoration: none;
}

.news_ins{
  text-align: center;
  
}

.news_ins_right{
  float: right;
}

.news_ins img{
  /* position: relative; */
  float: left;
  padding-left: 32px;
}

.news_ins pre{
  font-size: small;
  /* margin-top: 24dp; */
}

.news_ins h5{
  font-weight: 300;
}


</style>