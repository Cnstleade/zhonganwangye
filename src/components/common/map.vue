<template>
  <!--地图容器-->
  <div style="margin-bottom:100px">
       <div id="allmap" class="allmap">
         <img src="../../assets/img/map.png" alt="">
       </div>
  </div>
 
</template>
<script>
export default {
  name: "",
  data() {
    return {};
  },
  created: {},
  mounted() {
//     //     // 百度地图API功能
//     //     var map = new BMap.Map("allmap");
//     //     var poi = new BMap.Point(118.737493, 31.9889);
//     //     map.centerAndZoom(poi, 16);
//     //     map.enableScrollWheelZoom();

//     //     var content =
//     //       '<div style="margin:0;line-height:20px;padding:2px;">' +
//     //       '<img src="../img/baidu.jpg" alt="" style="float:right;zoom:1;overflow:hidden;width:100px;height:100px;margin-left:3px;"/>' +
//     //       "地址：北京市海淀区上地十街10号<br/>电话：(010)59928888<br/>简介：百度大厦位于北京市海淀区西二旗地铁站附近，为百度公司综合研发及办公总部。" +
//     //       "</div>";

//     //     //创建检索信息窗口对象
//     //     var searchInfoWindow = null;
//     //     searchInfoWindow = new BMapLib.SearchInfoWindow(map, content, {
//     //       title: "百度大厦", //标题
//     //       width: 290, //宽度
//     //       height: 105, //高度
//     //       panel: "panel", //检索结果面板
//     //       enableAutoPan: true, //自动平移
//     //       searchTypes: [
//     //         BMAPLIB_TAB_SEARCH, //周边检索
//     //         BMAPLIB_TAB_TO_HERE, //到这里去
//     //         BMAPLIB_TAB_FROM_HERE //从这里出发
//     //       ]
//     //     });
//     //     var marker = new BMap.Marker(poi); //创建marker对象
//     //     marker.enableDragging(); //marker可拖拽
//     //     marker.addEventListener("click", function(e) {
//     //       searchInfoWindow.open(marker);
//     //     });
//     //     map.addOverlay(marker); //在地图中添加marker
//     //     // searchInfoWindow.open(marker);
//     //     // console.log(searchInfoWindow.open(marker))
//     // var sContent =
//     //   "<h4 style='margin:0 0 5px 0;padding:0.2em 0'>中安投资租赁</h4>" +
//     //   "<img style='float:right;margin:4px' id='imgDemo' src='../../assets/img/hs.jpg' width='139' height='104' title='中安投资租赁'/>" +
//     //   "<p style='margin:0;line-height:1.5;font-size:13px;text-indent:2em'>中安投资租赁坐落在中国南京建邺区,新城科技园嘉陵江东街50号康缘智汇港11楼...</p>" +
//     //   "</div>";

    // setTimeout(() => {
    //   var map = new BMap.Map("allmap");
    //   var point = new BMap.Point(118.737493, 31.9889);
    //   var marker = new BMap.Marker(point);
    //   marker.setAnimation(BMAP_ANIMATION_BOUNCE);
    //   //var infoWindow = new BMap.InfoWindow(sContent); // 创建信息窗口对象
    //   map.centerAndZoom(point, 16);
    //   map.addOverlay(marker);
    //   map.enableScrollWheelZoom();
    //   marker.addEventListener("click", function() {
    //     this.openInfoWindow(infoWindow);
    //     //图片加载完毕重绘infowindow
    //     document.getElementById("imgDemo").onload = function() {
    //       infoWindow.redraw(); //防止在网速较慢，图片未加载时，生成的信息框高度比图片的总高度小，导致图片部分被隐藏
    //     };
    //   });
    // }, 20);
  }
};
</script>
<style scoped>
html,
body,
.allmap {
  height: 600px;
}
body,
html {
  width: 100%;
  height: 100%;
  margin: 0;
  font-family: "微软雅黑";
}
#allmap {
  height: 500px;
  width: 100%;
  overflow: hidden;
}
#result {
  width: 100%;
  font-size: 12px;
}
dl,
dt,
dd,
ul,
li {
  margin: 0;
  padding: 0;
  list-style: none;
}
dt {
  font-size: 14px;
  font-family: "微软雅黑";
  font-weight: bold;
  border-bottom: 1px dotted #000;
  padding: 5px 0 5px 5px;
  margin: 5px 0;
}
dd {
  padding: 5px 0 0 5px;
}
li {
  line-height: 28px;
}
</style>
