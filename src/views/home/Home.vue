<template>
  <div>
    <Navbar class="nav-bar">
      <div slot="center">蘑菇街</div>
    </Navbar>
    <HomeSwiper :banners="banner"></HomeSwiper>
    <home-recommend :recommend="recommend"></home-recommend>
    <HomePopular />
    <TabControl :titles="['流行','新款','精选']" class="tab-control"></TabControl>
    <ul>
      <li>占位列表1</li>
      <li>占位列表2</li>
      <li>占位列表3</li>
      <li>占位列表4</li>
      <li>占位列表5</li>
      <li>占位列表6</li>
      <li>占位列表7</li>
      <li>占位列表8</li>
      <li>占位列表9</li>
      <li>占位列表10</li>
      <li>占位列表11</li>
      <li>占位列表12</li>
      <li>占位列表13</li>
      <li>占位列表14</li>
      <li>占位列表15</li>
      <li>占位列表16</li>
      <li>占位列表17</li>
      <li>占位列表18</li>
      <li>占位列表19</li>
      <li>占位列表20</li>
      <li>占位列表21</li>
      <li>占位列表22</li>
      <li>占位列表23</li>
      <li>占位列表24</li>
      <li>占位列表25</li>
      <li>占位列表26</li>
      <li>占位列表27</li>
      <li>占位列表28</li>
      <li>占位列表29</li>
      <li>占位列表30</li>
      <li>占位列表31</li>
      <li>占位列表32</li>
      <li>占位列表33</li>
      <li>占位列表34</li>
      <li>占位列表35</li>
      <li>占位列表36</li>
      <li>占位列表37</li>
      <li>占位列表38</li>
      <li>占位列表39</li>
      <li>占位列表40</li>
      <li>占位列表41</li>
      <li>占位列表42</li>
      <li>占位列表43</li>
      <li>占位列表44</li>
      <li>占位列表45</li>
      <li>占位列表46</li>
      <li>占位列表47</li>
      <li>占位列表48</li>
      <li>占位列表49</li>
      <li>占位列表50</li>
    </ul>
  </div>
</template>

<script>
  //公共组件
import Navbar from '../../components/common/nav-bar/Navbar'
import TabControl from '../../components/content/tabControl/TabContyol'

  //home的子组件
import HomeSwiper from './children-components/HomeSwiper'
import {getHomeMultidata} from "../../network/home";
import HomeRecommend from './children-components/HomeRecommend'
import HomePopular from './children-components/HomePopular'

  export default {
    name: "Home",
    data(){
      return{
        banner:[],
        recommend:[]
      }
    },
    components:{
      Navbar,
      HomeSwiper,
      HomeRecommend,
      HomePopular,
      TabControl
    },
    created() {
      this.getHomeMultiData()
    },
    methods:{
      //网络请求相关的方法
      getHomeMultiData(){
        getHomeMultidata().then(res=>{
          this.banner =res.data.banner.list;
          this.recommend = res.data.recommend.list
        })
      }
      //常规事件处理的方法
    }
  }
</script>

<style scoped>
  .nav-bar{
    background: hotpink;
    font-size: 18px;
    font-weight:bold;
  }
  .tab-control{
    position: sticky;
    top: 44px;
    background: #fff;
  }
</style>


