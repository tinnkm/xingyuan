<template>
  <div class="wrapper" id="app">
    <Layout>
      <Header></Header>
      <Content class="content">
        <router-view></router-view>
      </Content>
      <Footer class="footer">2011-2016 &copy; TalkingData</Footer>
    </Layout>

  </div>
</template>

<script>
import Header from '@/components/Header.vue'
export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  min-height: 100vh;
  flex-direction: column;
}

.content{
  flex: 1;
  }
  .footer{
    flex: 0;
    height: 1.5rem;
    line-height: 1.5rem;
    vertical-align: middle;
  }

</style>
