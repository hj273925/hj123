运行步骤：
      //下载依赖
      npm install
      //运行服务
      npm run t_ibox
```
# 项目结构

```
.
├── build                                      // webpack配置文件
├── config                                     // 项目打包路径
├── src                                           // 源码目录
│   ├── assets                                      // 静态资源
│   ├── components                                  // 组件
│   ├── core                                        // 基本配置
│   │   ├── filters                                   // 过滤器
│   │   ├── mixins                                    // 混入
│   │   └── directives                                // 自定义指令
│   ├── router
│   │   └── index.js                                  // 路由配置
│   ├── service                                     // 数据交互统一调配
│   │   ├── api.service.js                            // 对请求进行统一的封装处理
│   │   └── .js                                       // 定义各个界面的请求
│   ├── store                                       // vuex的状态管理
│   │   ├── action.js                                 // 配置actions
│   │   ├── getters.js                                // 配置getters
│   │   ├── index.js                                  // 引用vuex，创建store
│   │   ├── modules                                   // store模块
│   │   └── mutations.js                              // 配置mutations
│   ├── App.vue                                     // 页面入口文件
│   ├── main.js                                     // 程序入口文件，加载各种公共组件
├── index.html                                  // 入口html文件
.


.
├── App.vue                    //项目入口
├── _nav.js                    //侧边菜单配置
├── assets                     //静态资源
|   |-- down.png
|   |-- font-icon
|   |   |-- iconfont.css
|   |   |-- iconfont.eot
|   |   |-- iconfont.svg
|   |   |-- iconfont.ttf
|   |   |-- iconfont.woff
|   |   -- iconfont.woff2
|   |-- icon
|   |   |-- clock.svg
|   |   |-- remind.svg
|   |   |-- stage.svg
|   |   `-- time.svg
|   |-- login
|   |   |-- Detection.png
|   |   |-- Operation.png
|   |   |-- Safety.png
|   |   |-- banner.png
|   |   `-- status.png
|   |-- login_logo.png
|   |-- logo.png
|   `-- scss
|       |-- _custom.scss
|       |-- _ie-fix.scss
|       |-- _variables.scss
|       |-- style.scss
|       `-- vendors
|           |-- _variables.scss
|           `-- chart.js
|               `-- chart.scss
|-- components                //组件
|   |-- ExportTable.vue
|   |-- SummaryCard.vue
|   |-- TableBar.vue
|   |-- TimeLine
|   |   |-- index.vue
|   |   `-- item.vue
|   |-- assetDetail.vue
|   |-- echarts                 //各种图表组件
|   |   |-- Bar.vue
|   |   |-- EventRanking.vue
|   |   |-- EventType.vue
|   |   |-- Pie.vue
|   |   |-- Radar.vue
|   |   |-- StackLine.vue
|   |   |-- WeekGeo.vue
|   |   `-- WeekLine.vue
|   `-- statusMonitor
|       |-- cardItem.vue
|       `-- labelFilter.js
|-- containers
|   |-- DefaultContainer.vue
|   `-- DefaultHeaderDropdownAccnt.vue
|-- init
|   |-- index.js
|   `-- vue-echarts.js
|-- main.js                    //初始化页面
|-- plugins                    //插件
|   |-- api.js
|   |-- confirm
|   |   |-- confirm.js
|   |   `-- index.vue
|   `-- table.js
|-- router                     //路由配置
|   |-- index.js
|   `-- router_config.js
|-- shared
|   `-- utils.js
|-- store.js                     //vuex配置
|-- utils                      //工具
|   |-- api.js                   //接口配置
|   |-- chart-mixin.js
|   |-- encrypt.js
|   |-- filter.js
|   |-- helper.js
|   |-- jurisdiction.js
|   |-- logger.js
|   |-- plugins.js
|   |-- promise.js
|   |-- table-mixin.js           //表格共用的基础配置
|   |-- tableColumns.js          //各页面表格配置
|   |-- typeFilter.js
|   |-- typeMap.js
|   |-- util.js
|   `-- validator.js
`-- views                //路由视图
    |-- Alert.vue
    |-- Asset                 //资产信息
    |   |-- Android             //安卓
    |   |   `-- index.vue
    |   |-- AssetAPN.vue
    |   |-- AssetAPP.vue
    |   |-- AssetDetail.vue
    |   |-- AssetTags.vue
    |   |-- Ibox                //Ibox
    |   |   `-- index.vue
    |   |-- PermissionList.vue
    |   |-- TagManagement.vue
    |   |-- detailColumns.js
    |   `-- statusMonitor       //资产状态
    |       `-- index.vue
    |-- Charts.vue
    |-- Dashboard.vue
    |-- DetectionVulnerability
    |   `-- index.vue
    |-- IntrusionDetection   //入侵检测
    |   |-- AccountMonitoring  //账号监控
    |   |   `-- index.vue
    |   |-- DetectionResult    //应用检测
    |   |   |-- DetectionDetail.vue
    |   |   `-- index.vue
    |   |-- FileMonitoring     //文件监控
    |   |   `-- index.vue
    |   |-- NetworkMonitoring  //日志监控
    |   |   `-- index.vue
    |   |-- PortScan           //端口扫描
    |   |   `-- index.vue
    |   |-- PortSnapshot       //端口监控
    |   |   `-- index.vue
    |   |-- ProcessSnapshot    //进程监控
    |   |   `-- index.vue
    |   |-- Root               //root提权
    |   |   `-- index.vue
    |   |-- TimingMonitoring   //定时任务监控
    |   |   `-- index.vue
    |   `-- UsbTest            //usb检测
    |       `-- index.vue
    |-- Logservice           //日志服务
    |   |-- AuditingOperation  //审计操作
    |   |   `-- index.vue
    |   |-- SecurityAudit      //系统审计
    |   |   |-- index.vue
    |   |   `-- recordList.js
    |   `-- SystemLog          //系统日志
    |       `-- index.vue
    |-- MapQuery
    |   `-- index.vue
    |-- Nssa                   //态势感知
    |   |-- HorizontalBar.vue
    |   |-- Ktable.vue
    |   |-- SecurityTrend.vue
    |   |-- ThreatDistribution.vue
    |   |-- ThreatLevel.vue
    |   |-- eventTable.vue
    |   `-- index.vue
    |-- RemoteOperation        //远程操作
    |   |-- CommandPush        //命令推送
    |   |   |-- CommandDetail.vue
    |   |   |-- CommandIssuance.vue
    |   |   |-- CommandList.vue
    |   |   `-- index.vue
    |   `-- Sota               //SOTA升级
    |       |-- AddSota.vue
    |       |-- SotaList.vue
    |       `-- index.vue
    |-- SecurityEvents         //安全事件
    |   |-- detail.vue
    |   |-- detailColumns.js
    |   |-- eventDetailColumns.js
    |   |-- filterMenu.js
    |   |-- filterMenu.vue
    |   `-- index.vue
    |-- System                 //系统设置
    |   |-- IdleSetting.vue
    |   |-- UserManage.vue
    |   |-- UserPasswd.vue
    |   `-- index.vue
    |-- VehicleDetection     //网络安全
    |   |-- BluetoothDetection //蓝牙监控
    |   |   `-- index.vue
    |   `-- WifiDetection      //WIFI监控
    |       `-- index.vue
    `-- login                  //登录
        |-- Login.vue
        `-- container.js
.
