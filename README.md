# Sexy Donate

[![HexoOptimized](https://img.shields.io/badge/HEXO-Optimized-orange.svg)](https://hexo.io)
[![README](https://img.shields.io/badge/README-Chinese-blue.svg)](https://github.com/spencerwoo98/sexy-donate/blob/master/README-zh.md)
![Packagist](https://img.shields.io/packagist/l/doctrine/orm.svg?style=flat)
[![HitCount](http://hits.dwyl.io/spencerwoo98/sexy-donate.svg)](http://hits.dwyl.io/spencerwoo98/sexy-donate)

![img](https://i.loli.net/2018/03/14/5aa8c027b2460.gif)

An extremely lightweight donation system for static webpages.

So lightweight that it:

- Does not require any server-side implementation.
- Consists of no more than 100 lines of code.
- Can easily blend in any theme or static webpages without destroying its integrity.

The snippet was intended for [hexo](https://hexo.io).

Click here for a detailed -> [DEMO](https://spencerwoo.com).

# Let's Get Started

## 1. Installation

``` html
<link rel="stylesheet" href="https://spencerwoo.com/css/donate.css">
<script src="https://cdn.bootcss.com/jquery/3.3.1/core.js"></script>
<script src="https://spencerwoo.com/js/donate.js"></script>
```
Put all of above in the `<head></head>` partition of your page. As for my theme, it is in `_partial/head.ejs`.
These are the requirements of SexyDonate.

## 2. Render Sexy Donate Container
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
Put **ALL OF ABOVE** to the end of your post, above your comments area.

As for me, it is in the file `post.ejs`. Customize according to your own hexo theme or static webpage.

Do change all content between the `$...$`, as in your own text shown in the button, your own WeChat Donation QR Code and your own AliPay QR Code.

The QR Code image require a bit of tweaking, I suggest you upload your generated QR Code onto a Image Hosting Website. Then paste the URL into `src="$HERE$"`

I do appreciate it if you would keep the `powered_text` `<div>`. Huge Thanks.

## 3. Finalize
In your terminal, navigate to your root hexo blog folder, and run the following script:
```shell
hexo clean && hexo d -g
```
Now go to your blog and see what happened! :smile:

# Dependencies

- jQuery 3.3.1

- Button wobble effect by [Animista](http://animista.net/)

![img](https://i.loli.net/2018/03/14/5aa8bc4b20774.jpg)

# TO-DO

- Use Javascript to render the HTML snippets for single-line usage.
- ~~Add wobble effect for the button.~~
- ~~Add Chinese Version README~~

# License

[MIT License](https://opensource.org/licenses/MIT)
