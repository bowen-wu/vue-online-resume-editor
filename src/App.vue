<template>
  <div id="app">
    <Topbar class="topbar"/>
    <main>
      <Editor class="editor"/>
      <Preview class="preview"/>
    </main>
  </div>
</template>

<script>
import Topbar from './components/Topbar'
import Editor from './components/Editor'
import Preview from './components/Preview'

export default {
  name: 'App',
  components: {
    Topbar, Editor, Preview, 
  }
}
</script>

<style lang="scss">
@mixin flex($justifyContent, $alignItems){
  display: flex;
  justify-content: $justifyContent;
  align-items: $alignItems;
}
#app {
  height: 100vh;
  @include flex(none, none);
  flex-direction: column;
  background-color: #EEEEEE;
  >.topbar{
    height: 60px;
    background-color: #fff;
  }
  >main{
    flex: 1;
    @include flex(none, none);
    >.editor{
      width: 200px;
    }
    >.preview{
      flex: 1;
    }
  }
}
</style>
