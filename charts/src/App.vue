<template>
  <div class=page>
   <header>
    <Topbar/>
   </header>
   <main>
    <ResumeEditor/>
    <ResumePreview/>
   </main>
  </div>
</template>

<script>
import 'normalize.css/normalize.css'
import './assets/reset.css'

import Topbar from './components/Topbar'
import ResumeEditor from './components/ResumeEditor'
import ResumePreview from './components/ResumePreview'
import store from './store/index'

export default {
  name: 'app',
  store,
  components:{Topbar,ResumeEditor,ResumePreview}
}
</script>

<style lang="scss">
.page{
  height:100vh;
  display:flex;
  flex-direction:column;
  background:#d4d9dd;

>main{
  flex-grow:1;
}
>main{
  min-width:1024px;
  max-width:1440px;
  margin-top:16px;
  margin-bottom:16px;
  display:flex;
  justify-content:space-between;
  padding:0 16px;
  width:100%;
  align-self:center;
 }
}
#resumeEditor{
  min-width:27%;
  background:#444;
}
#resumePreview{
  flex-grow:1;
  margin-left:33px;
  background:#777;
}
</style>
