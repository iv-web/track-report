
##track report

#### Usage:

##### import:

js file `/lib/index.js`

<scrpt src="xxxxx/lob/index.js"></scrpt>

##### config:

```js
BJ_REPORT.init({
    id: 0, // 上报 id
    uin: 0, // user id
    url: "", // 上报 接口
    offline_url: "", // 离线日志上报 接口
    offline_auto_url: "", // 检测是否自动上报
    ext: null, // 扩展参数 用于自定义上报
    level: 4, // 错误级别 1-debug 2-info 4-error 20 offlinelog
    ignore: [], // 忽略某个错误, 支持 Regexp 和 Function
    random: 1, // 抽样 (0-1] 1-全量
    delay: 1000, // 延迟上报 combo 为 true 时有效
    submit: null, // 自定义上报方式
    repeat: 5 , // 重复上报次数(对于同一个错误超过多少次不上报),
    offlineLog : true, // 是否启用了离线日志
    offlineLogExp : 5,  // 离线日志过期时间 ， 默认5天
    offlineLogAuto : true,  //是否自动询问服务器需要自动上报
})
```

window.onerror will be overwrite to catch javascript error and report to server.

#### API:

1 report a msg

BJ_REPORT.report(msg)

2 report a info msg

BJ_REPORT.info(msg)


3 report a debug msg

BJ_REPORT.debug(msg)

4 report a offline log

BJ_REPORT.offlineLog(msg)


