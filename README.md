# bootstrap
##整体页面预览

![](https://github.com/lc-dmx/bootstrap/blob/master/%E7%8E%B0%E4%BB%A3%E6%B5%8F%E8%A7%88%E5%99%A8%E5%8D%9A%E7%89%A9%E9%A6%86.png)

##bootstrap页面尺寸改变效果

![](https://github.com/lc-dmx/bootstrap/blob/master/%E7%AA%97%E5%8F%A3%E7%BC%A9%E5%B0%8F.jpg)

##轮播效果

![](https://github.com/lc-dmx/bootstrap/blob/master/%E8%BD%AE%E6%92%AD.jpg)

```html
<div id="ad-carousel" class="carousel slide" data-ride="carousel">
       <ol class="carousel-indicators">
         <li data-target="#ad-carousel" data-slide-to="0" class="active"></li>
         <li data-target="#ad-carousel" data-slide-to="1"></li>
         <li data-target="#ad-carousel" data-slide-to="2"></li>
         <li data-target="#ad-carousel" data-slide-to="3"></li>
         <li data-target="#ad-carousel" data-slide-to="4"></li>
       </ol>
       <div class="carousel-inner" role="listbox">
          <div class="active item">
            <img src="images/chrome-big.jpg" alt="1 slide">

            <div class="container">
              <div class="carousel-caption">
                <h1>Chrome</h1>

                    <p>Google Chrome，又称Google浏览器，是一个由Google（谷歌）公司开发的网页浏览器。</p>

                    <p><a class="btn btn-lg btn-primary" href="http://www.google.cn/intl/zh-CN/chrome/browser/"
                          role="button" target="_blank">点我下载</a></p>
              </div>
            </div>
          </div>
          <div class="item" >
            <img src="images/firefox-big.jpg" alt="2 slide">

            <div class="container">
              <div class="carousel-caption">
                <h1>Firefox</h1>

                    <p>Mozilla Firefox，中文名通常称为“火狐”或“火狐浏览器”，是一个开源网页浏览器。</p>

                    <p><a class="btn btn-lg btn-primary" href="http://www.firefox.com.cn/download/" target="_blank"
                          role="button">点我下载</a></p>
              </div>
            </div>
          </div>
          <div class="item" >
            <img src="images/safari-big.jpg" alt="3 slide">

            <div class="container">
              <div class="carousel-caption">
                <h1>Safari</h1>

                    <p>Safari，是苹果计算机的最新操作系统Mac OS X中的浏览器。</p>

                    <p><a class="btn btn-lg btn-primary" href="http://www.apple.com/cn/safari/" target="_blank"
                          role="button">点我下载</a></p>
              </div>
            </div>
          </div>
          
       </div>
       <a class="carousel-control left" href="#ad-carousel" role="button" data-slide="prev">
         <span class="glyphicon glyphicon-chevron-left"></span>
         <span class="sr-only">Previous</span>
       </a>
       <a class="carousel-control right" href="#ad-carousel" role="button" data-slide="next">
         <span class="glyphicon glyphicon-chevron-right"></span>
         <span class="sr-only">Next</span>
       </a>
  </div>
```

##下拉框

![](https://github.com/lc-dmx/bootstrap/blob/master/%E4%B8%8B%E6%8B%89%E6%A1%86.jpg)

```html
<nav class="navbar navbar-default navbar-fixed-top " role="navigation" id="menu-nav">
  <div class="navbar-collapse" id="demo-navbar">
    <li class="dropdown">
      <a href="#" class="dropdown-toggle" data-toggle="dropdown">特点<span class="caret"></span></a>
        <ul class="dropdown-menu" role="menu">
          <li><a href="#feature-tab" data-tab="tab-chrome">Chrome</a></li>
          <li><a href="#feature-tab" data-tab="tab-firefox">Firefox</a></li>
          <li><a href="#feature-tab" data-tab="tab-safari">Opera</a></li>
        </ul>
    </li>
  </div>

    <ul class="nav nav-tabs" role="tablist" id="feature-tab">
      <li class="active"><a href="#tab-chrome" role="tab" data-toggle="tab">Chrome</a></li>
      <li><a href="#tab-firefox" role="tab" data-toggle="tab">Firefox</a></li>
      <li><a href="#tab-safari" role="tab" data-toggle="tab">Safari</a></li>
    </ul>
    <div class="tab-content">
        <div class="tab-pane active" id="tab-chrome">
            <div class="row feature">
                <div class="col-md-7">

                    <h2 class="feature-heading">Google Chrome <span
                            class="text-muted">使用最广的浏览器</span></h2>

                    <p class="lead">Google Chrome，又称Google浏览器，是一个由Google（谷歌）公司开发的网页浏览器。
                        该浏览器是基于其他开源软件所撰写，包括WebKit，目标是提升稳定性、速度和安全性，并创造出简单且有效率的使用者界面。</p>
                </div>
                <div class="col-md-5">
                    <img class="feature-image img-responsive" src="images/chrome-logo.jpg"
                         alt="Chrome">
                </div>
            </div>
        </div>
    </div>
```
```javascript
<script>
    $(function () {
        $('#ad-carousel').carousel();
        $('#menu-nav .navbar-collapse a').click(function (e) {
            var href = $(this).attr('href');
            var tabId = $(this).attr('data-tab');
            if ('#' !== href) {
                e.preventDefault();
                $(document).scrollTop($(href).offset().top - 70);
                if (tabId) {
                    $('#feature-tab a[href=#' + tabId + ']').tab('show');
                }
            }
        });
    });
</script>
```

##弹出框

![](https://github.com/lc-dmx/bootstrap/blob/master/%E5%BC%B9%E5%87%BA%E6%A1%86.jpg)

```html
 <div class="modal fade" id="about-modal" tabindex="-1" role="dialog" aria-labelledby="modal-label"
         aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <button type="button" class="close" data-dismiss="modal"><span
                            aria-hidden="true">&times;</span><span class="sr-only">关闭</span></button>
                    <h4 class="modal-title" id="modal-label">关于</h4>
                </div>
                <div class="modal-body">
                    <p>好好学习，天天向上</p>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-default" data-dismiss="modal">了解了</button>
                </div>
            </div>
        </div>
    </div>
```
