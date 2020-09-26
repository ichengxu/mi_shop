<template>
  <div class="header">
    <div class="nav-topbar">
      <div class="container">
        <div class="topbar-menu">
          <a href="javascript:;">小米商城</a>
          <a href="javascript:;">MUI</a>
          <a href="javascript:;">云服务</a>
          <a href="javascript:;">协议规则</a>
        </div>
        <div class="topbar-user">
          <a href="javascript:;" @click="login">登录</a>
          <a href="/#/order/list" v-if="username">我的订单</a>
          <a href="javascript:;" class="my-cart" @click="goToCart"><span class="icon-cart"></span>购物车({{cartCount}})</a>
        </div>
      </div>
    </div>
    <div class="nav-header">
      <div class="container">
        <div class="header-logo">
          <a href="/#/index"></a>
        </div>
        <div class="header-menu">
          <div class="item-menu">
            <span>小米手机</span>
            <div class="children">
              <ul>
                <li class="product">
                  <a href="/#/product/31" target="_blank">
                    <div class="pro-img"><img src="/imgs/nav-img/nav-1.png" alt=""></div>
                    <div class="pro-name">小米CC9</div>
                    <div class="pro-price">1799元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="/#/product/31" target="_blank">
                    <div class="pro-img"><img src="/imgs/nav-img/nav-1.png" alt=""></div>
                    <div class="pro-name">小米CC9</div>
                    <div class="pro-price">1799元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="/#/product/31" target="_blank">
                    <div class="pro-img"><img src="/imgs/nav-img/nav-1.png" alt=""></div>
                    <div class="pro-name">小米CC9</div>
                    <div class="pro-price">1799元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="/#/product/31" target="_blank">
                    <div class="pro-img"><img src="/imgs/nav-img/nav-1.png" alt=""></div>
                    <div class="pro-name">小米CC9</div>
                    <div class="pro-price">1799元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="/#/product/31" target="_blank">
                    <div class="pro-img"><img src="/imgs/nav-img/nav-1.png" alt=""></div>
                    <div class="pro-name">小米CC9</div>
                    <div class="pro-price">1799元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="/#/product/31" target="_blank">
                    <div class="pro-img"><img src="/imgs/nav-img/nav-1.png" alt=""></div>
                    <div class="pro-name">小米CC9</div>
                    <div class="pro-price">1799元</div>
                  </a>
                </li>
              </ul>
            </div>
          </div>
          <div class="item-menu">
            <span>RedMi红米</span>
          </div>
          <div class="item-menu">
            <span>电视</span>
            <div class="children">
              <ul>
                <li class="product">
                  <a href="" target="_blank">
                    <div class="pro-img">
                      <img v-lazy="'/imgs/nav-img/nav-3-1.jpg'" alt="">
                    </div>
                    <div class="pro-name">小米壁画电视 65英寸</div>
                    <div class="pro-price">6999元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="" target="_blank">
                    <div class="pro-img">
                      <img v-lazy="'/imgs/nav-img/nav-3-2.jpg'" alt="">
                    </div>
                    <div class="pro-name">小米全面屏电视E55A</div>
                    <div class="pro-price">1999元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="" target="_blank">
                    <div class="pro-img">
                      <img v-lazy="'/imgs/nav-img/nav-3-3.png'" alt="">
                    </div>
                    <div class="pro-name">小米电视4A 32英寸</div>
                    <div class="pro-price">699元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="" target="_blank">
                    <div class="pro-img">
                      <img v-lazy="'/imgs/nav-img/nav-3-4.jpg'" alt="">
                    </div>
                    <div class="pro-name">小米电视4A 55英寸</div>
                    <div class="pro-price">1799元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="" target="_blank">
                    <div class="pro-img">
                      <img v-lazy="'/imgs/nav-img/nav-3-5.jpg'" alt="">
                    </div>
                    <div class="pro-name">小米电视4A 65英寸</div>
                    <div class="pro-price">2699元</div>
                  </a>
                </li>
                <li class="product">
                  <a href="" target="_blank">
                    <div class="pro-img">
                      <img v-lazy="'/imgs/nav-img/nav-3-6.png'" alt="">
                    </div>
                    <div class="pro-name">查看全部</div>
                    <div class="pro-price">查看全部</div>
                  </a>
                </li>
                
              </ul>
            </div>
          </div>
          <div class="item-menu">
							<span>笔记本</span>
							<div class="children">
								<!-- 当鼠标移到上面得span标题得时候children才会被展示出来。移开之后children会被隐藏掉-->
								
								<ul>
									<!-- 为什么使用li标签: 如果需要循环得话li标签是最合适得因为li刚好是一个对称得结果可以无限循环下去-->
									<!-- 每一个li标签就是每一个商品 -->
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										<!-- 通过高度设置为0去隐藏 -->
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>

									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										<!-- 如果右边得线与li高度不相等。这就不能通过border-right去设置。最优是通过伪类after去实现 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
								</ul>
							</div>
						</div>

						<div class="item-menu">
							<span>家电</span>
							<div class="children">
								<!-- 当鼠标移到上面得span标题得时候children才会被展示出来。移开之后children会被隐藏掉-->
								
								<ul>
									<!-- 为什么使用li标签: 如果需要循环得话li标签是最合适得因为li刚好是一个对称得结果可以无限循环下去-->
									<!-- 每一个li标签就是每一个商品 -->
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										<!-- 通过高度设置为0去隐藏 -->
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>

									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										<!-- 如果右边得线与li高度不相等。这就不能通过border-right去设置。最优是通过伪类after去实现 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
								</ul>
							</div>
						</div>

						<div class="item-menu">
							<span>路由器</span>
							<div class="children">
								<!-- 当鼠标移到上面得span标题得时候children才会被展示出来。移开之后children会被隐藏掉-->
								
								<ul>
									<!-- 为什么使用li标签: 如果需要循环得话li标签是最合适得因为li刚好是一个对称得结果可以无限循环下去-->
									<!-- 每一个li标签就是每一个商品 -->
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										<!-- 通过高度设置为0去隐藏 -->
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>

									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										<!-- 如果右边得线与li高度不相等。这就不能通过border-right去设置。最优是通过伪类after去实现 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
									<li class="product">
										<!-- 每个li标签都分为3块内容：图片、标题、价格 -->
										<!-- 因为是可以点击跳转到相对于得产品站得所以这里选为a标签用a标签包裹即可 -->
										<!-- 当然如果让li跳转也可以通过window.open -->
										<!-- 布局本着先布局大结构在布局小结构 -->
										
										<a href="javascript:;" target="_blank">
											<div class="pro-img">
												<!-- 图片 -->
												<!-- 图片得宽或者高只能设置一个让另一个去自适应。如果都设置会导致压缩变形 -->
												<img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3bf20f1df3f2e22c5b29ff07634f3c59.png?thumb=1&w=160&h=110&f=webp&q=90">	
											</div>	
											<div class="pro-name">
												<!-- 标题 -->
												小米10 青春版 5G
											</div>
											<div class="pro-price">
												<!-- 价格 -->
												2099元起
											</div>
										</a>
									</li>
								</ul>
							</div>
						</div>

        </div>
        <div class="header-search">
          <div class="wrapper">
            <input type="text" name="keyword">
            <a href="javascript:;"></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default{
    name:'nav-header',
    methods:{
      login(){
        this.$router.push('/login');
      },
      goToCart(){
        this.$router.push('/cart');
      }
    }
  }
</script>
<style lang="scss">
  @import './../assets/scss/base.scss';
  @import './../assets/scss/mixin.scss';
  @import './../assets/scss/config.scss';
  .header{
    .nav-topbar{
      height:39px;
      line-height:39px;
      background-color:#333333;
      color:#B0B0B0;
      .container{
        @include flex();
        a{
          display:inline-block;
          color:#B0B0B0;
          margin-right:17px;
        }
        .my-cart{
          width:110px;
          background-color:#FF6600;
          text-align:center;
          color:#ffffff;
          margin-right:0;
          .icon-cart{
            @include bgImg(16px,12px,'/imgs/icon-cart-checked.png');
            margin-right:4px;
          }
        }
      }
    }
    .nav-header{
      .container{
        position:relative;
        height:112px;
        @include flex();
        .header-menu{
          display:inline-block;
          width:643px;
          padding-left:209px;
          .item-menu{
            display:inline-block;
            color:#333333;
            font-weight:bold;
            font-size:16px;
            line-height:112px;
            margin-right:20px;
            span{
              cursor:pointer;
            }
            &:hover{
              color:$colorA;
              .children{
                height:220px;
                opacity:1;
              }
            }
            .children{
              position:absolute;
              top:112px;
              left:0;
              width:1226px;
              height:0;
              opacity:0;
              overflow:hidden;
              border-top:1px solid #E5E5E5;
              box-shadow:0px 7px 6px 0px rgba(0, 0, 0, 0.11);
              z-index: 10;
              transition:all .5s;
              background-color: #ffffff;
              .product{
                position:relative;
                float:left;
                width:16.6%;
                height:220px;
                font-size:12px;
                line-height:12px;
                text-align: center;
                a{
                  display:inline-block;
                }
                img{
                  width:auto;
                  height:111px;
                  margin-top:26px;
                }
                .pro-img{
                  height:137px;
                }
                .pro-name{
                  font-weight:bold;
                  margin-top:19px;
                  margin-bottom:8px;
                  color:$colorB;
                }
                .pro-price{
                  color:$colorA;
                }
                &:before{
                  content:' ';
                  position:absolute;
                  top:28px;
                  right:0;
                  border-left:1px solid $colorF;
                  height:100px;
                  width:1px;
                }
                &:last-child:before{
                  display:none;
                }
              }
            }
          }
        }
        .header-search{
          width:319px;
          .wrapper{
            height:50px;
            border:1px solid #E0E0E0;
            display:flex;
            align-items:center;
            input{
              border:none;
              box-sizing: border-box;
              border-right:1px solid #E0E0E0;
              width:264px;
              height:50px;
              padding-left:14px;
            }
            a{
              @include bgImg(18px,18px,'/imgs/icon-search.png');
              margin-left:17px;
            }
          }
        }
      }
    }
  }
</style>