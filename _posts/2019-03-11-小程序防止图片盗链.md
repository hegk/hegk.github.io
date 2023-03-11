---
layout: post
title: 微信小程序中 -- 防止图片盗链
date: 2019-03-11 12:00:00.000000001 +08:00
---

今天在写微信小程序的时候，copy了小程序demo的一段代码，做测试,这个是给swiper写的一组数据源
```
data: {
    imgUrls: [
      'http://img02.tooopen.com/images/20150928/tooopen_sy_143912755726.jpg',
      'http://img06.tooopen.com/images/20160818/tooopen_sy_175866434296.jpg',
      'http://img06.tooopen.com/images/20160818/tooopen_sy_175833047715.jpg'
    ],
    indicatorDots: false,
    autoplay: false,
    interval: 5000,
    duration: 1000
  }
```

在跑起来的时候，总是在console中打印一组
<image src="https://github.com/Fe7s/Fe7s.github.io/blob/master/assets/iamgesList/Summary/防止图片盗链.png?raw=true"></image>

这个原因就是防止图片盗链导致的，此时需要把demo里买呢url换成自己的，这样就没事了

#### [盗链](https://baike.baidu.com/item/%E7%9B%97%E9%93%BE/4934434)
    盗链是指服务提供商自己不提供服务的内容，通过技术手段绕过其它有利益的最终用户界面（如广告），直接在自己的网站上向最终用户提供其它服务提供商的服务内容，骗取最终用户的浏览和点击率。受益者不提供资源或提供很少的资源，而真正的服务提供商却得不到任何的收益。



