<template>
  <div class="top-nav">
    <span>프로모션 개발팀</span>
    <span>업무 시스템</span>
    <span>기획파트_최재민님</span>
    <button>개인 실적</button>
    <button>로그아웃</button>
  </div>
  
  <div class="contents">
    <nav class="side-nav">
    <router-link to="/">업무 현황</router-link>
    <router-link to="/team">업무보고서_팀 전체</router-link>
    <router-link to="/part">업무보고서_파트별</router-link> 
    <router-link to="/personal">업무보고서_개인별</router-link>

  </nav>
  <router-view class="content"/>
  </div>
</template>

<style lang="scss">
.top-nav{
  display: flex;
  justify-content: space-between;
  font-weight: bold;
  font-size: 15px;
  padding: 10px;
  border-bottom:1px solid gray ;
  :nth-child(2){
    padding-left: 15px;
  }
  :nth-child(3){
    padding-left: 1200px;
  }
  :nth-child(4){
    padding-left: 15px;
  }
  :nth-child(5){
    padding-left: -15px;
  }
}
.contents{
  display: flex;
}
.side-nav{
  display: flex;
  flex-direction: column; 
  height:100vh;
  border-right:1px solid gray ;
}
.content{
  width:100%;
}


nav {
  padding:8px;
}

nav a {
  width: 145px;
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
