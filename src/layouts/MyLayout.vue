<template>
  <q-layout view="lHh Lpr lFf">
  <q-layout-body>
    <head>
      <link rel="stylesheet" href="/css/style.css">
    </head>
    <body>

    <h5>待認養寵物</h5>
   
    <!-- Lesson 2. Forms 表單 -->
    <form action="mailto:yooomain@gmail.com" method="post" enctype="text/plain">
      <label for="Search">搜尋姓名</label>
      <input type="text" name="name"><br>
      <label>進階搜尋</label> 
      <textarea name="moresearch" id="" cols="10" rows="2"></textarea><br>
      <input type="submit">
    </form>
    <!-- Forms End -->
    
    <hr>
     <!--Lesson 1. HTML - table  -->
      <table>
        <!-- th=thead 標題 tr= table row td=table data -->
        <thead>
        <tr>
          <th>姓名</th>
          <th>可愛照片</th>
          <th>聯絡飼主</th>
        </tr>
        </thead>

        <tbody>
          <tr>
            <td>A</td>
            <td><img src="/assets/EGG.png"></td>
            <td><a href="/pages/Index.vue" target="_blank">A聯絡人</a></td>
         </tr>
         <tr>
           <td>B</td>
           <td><img src="/assets/EGG.png"></td>
          <td><a href="https://www.google.com.tw/?gws_rd=ssl" target="_blank">B聯絡人</a></td>
         </tr>
        </tbody>
        <tfoot>
          
        </tfoot>
        
      </table>
      地方貓咪需要您的幫忙!
    
    <!-- table End -->
  </body>
  </q-layout-body>
 

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',   
  data () {
    return {
      leftDrawerOpen: false
    }
  },
  methods: {
    openURL
  }
}
</script>

<style>
body{
  color:blue; 
}
</style>
