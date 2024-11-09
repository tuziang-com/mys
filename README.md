# 绵阳市专业技术人员继续教育


## 脚本

学习网站：
绵阳市人力资源和社会保障局: https://rsj.my.gov.cn/  
绵阳市专业技术人员继续教育公需科目培训平台: https://rsjapp.mianyang.cn/jxjy/pc/index.jhtml

脚本地址：[绵阳市专业技术人员继续教育-刷课脚本][2]

## 教程

浏览器安装篡改猴插件后，打开[脚本安装地址][2]，进入后点击安装脚本，安装完成刷新你的学习网页就可以愉快使用了。

## 联系

注：如果需要代学，可以联系我微信yizhituziang或者QQ2422270452

![微信二维码](https://www.tuziang.com/wx.jpg)

## 更多

关键代码分享：
```

  // 判断播放完成后下一节
  setInterval(function () {
    var text = $('.title.active').text()
    if (text.indexOf("【已完成】") != -1) {
      for (let i = 0; i < $('#main > div.content > div > div.courseAction_lesson_left.lesson_left > div.list > div > ul > li').length; i++) {
        let liItem = $('#main > div.content > div > div.courseAction_lesson_left.lesson_left > div.list > div > ul > li')[i]
        if (liItem.textContent.indexOf("未完成") != -1) {
          liItem.click()
        }
      }
    }
  }, 1000)

  // 自动点击继续播放
  setInterval(function () {
    if ($('#jAlertContent > p').length == 1) {
      $('#jAlertButton2').click()
    }
  }, 1000)

  // 确保视频在播放状态
  setInterval(function () {
    document.getElementsByTagName("video")[0].muted = true
    document.getElementsByTagName("video")[0].play()
  }, 100)
```


  [1]: https://microsoftedge.microsoft.com/addons/detail/%E7%AF%A1%E6%94%B9%E7%8C%B4/iikmkjmpaadaobahmlepeloendndfphd?refid=bingshortanswersdownload
  [2]: https://greasyfork.org/zh-CN/scripts/505418-%E4%B8%BD%E6%B0%B4%E4%BA%BA%E7%A4%BE%E5%85%AC%E9%9C%80%E7%A7%91%E7%9B%AE%E5%88%B7%E8%AF%BE%E8%84%9A%E6%9C%AC-%E8%87%AA%E5%8A%A8%E5%AD%A6%E4%B9%A0
