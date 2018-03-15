# Sexy Donate 阳阳打赏

[![HexoOptimized](https://img.shields.io/badge/HEXO-Optimized-orange.svg)](https://hexo.io)
[![README](https://img.shields.io/badge/README-Chinese-blue.svg)](https://github.com/spencerwoo98/sexy-donate/blob/master/README-zh.md)
![Packagist](https://img.shields.io/packagist/l/doctrine/orm.svg?style=flat)
[![HitCount](http://hits.dwyl.io/spencerwoo98/sexy-donate.svg)](http://hits.dwyl.io/spencerwoo98/sexy-donate)

![img](https://i.loli.net/2018/03/14/5aa8c027b2460.gif)

一款极为简单轻便的打赏系统，专为静态网页准备。

何为轻便？

- 「阳阳打赏」无需任何服务端配置
- 不到 100 行代码即可实现打赏按钮
- 可以完美嵌入任何简洁的 Hexo 主题

代码已为 [Hexo](https://hexo.io) 专门优化.

点击这里查看 -> [DEMO](https://spencerwoo.com).

# 来，兄弟，上车吧

## 1. 安装

``` html
<link rel="stylesheet" href="https://spencerwoo.com/css/donate.css">
<script src="https://cdn.bootcss.com/jquery/3.3.1/core.js"></script>
<script src="https://spencerwoo.com/js/donate.js"></script>
```
将以上所有代码放入 Hexo 页面的 `<head></head>` 部分。我的主题定义的在 `_partial/head.ejs`.
这些是「阳阳打赏」的依托。

## 2. 生成「阳阳打赏」Fragment
```html
<div class="post_reward">
    <label class="reward_btn">$请喝咖啡$</label>
    <div class="qr_code">
        <div class="qr_code_img">
            <img class="image" src="$Path_To_Your_WechatDonationCode$" title="WeChat">
        </div>

        <div class="qr_code_img">
            <img class="image" src="$Path_To_Your_AlipayDonationCode$" title="AliPay">
        </div>
    </div>

    <div class="powered_text">
        Powered by <a href="https://github.com/spencerwoo98/sexy-donate">SexyDonate</a>
    </div>
</div>

```
将 **以上所有代码** 放到 hexo 的 post 页面每篇博文下，comment 部分以上。

我的主题在`post.ejs`文件中。

将`$...$`中间的部分全部更改，分别改成：
1. 你想要的按钮显示文本，比如：「打赏吗兄弟？」「按一下又不会怀孕！」
2. 你自己的微信支付打赏二维码图片外链
3. 你自己的支付宝支付打赏二维码图片外链

**附：图片外链**
建议你将用微信和支付宝生成的打赏二维码进行上传至国内某图床，以加速访问速度。推荐图床有：
- 七牛云：
    - 优点：国内，稳定靠谱且便宜，个人博客仅需不到 1 RMB 一个月。
    - 缺点：未备案的域名只支持 `http` 访问。
- SM.MS:
    - 优点：支持 `https` 访问。
    - 缺点：没有后台登录系统，一旦上传，需要根据返回 `json` 进行删除文件。

之后将你得到的图片外链粘贴至 `src="$HERE$"` 这里。
如果你并没有删掉后面的 `powered_text` 部分，那我将十分感谢您。

## 3. 收尾
在终端中，`cd` 到您的 hexo 根目录，然后运行：
```shell
hexo clean && hexo d -g
```
现在去你的网站看看效果吧！:smile:

# 依托

- jQuery 3.3.1

- Button wobble effect by [Animista](http://animista.net/)

![img](https://i.loli.net/2018/03/14/5aa8bc4b20774.jpg)

# 接下来...

- Use Javascript to render the HTML snippets for single-line usage.
- ~~Add wobble effect for the button.~~
- ~~Add Chinese Version README~~

# 许可

[MIT License](https://opensource.org/licenses/MIT)
