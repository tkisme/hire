# 答案1

- angular的好处很多,但是学习成本高,代码维护代价高,调试难度高,再加上不够成熟
- 目前你们的源代码中还是有很多的优化可以做,比如在
https://static11.elemecdn.com/eleme/desktop/main.55de3a.js
中最后一行
i='<div checkout-guide guide=guide></div><div loading ng-if=loading></div><div class="ordersuccess pay-header container" ng-show=!loading><i class="icon-circle-check pay-header-icon"></i><div class=pay-header-info><h2 ng-if=order.is_online_paid>订单已成功提交并付款，请耐心等待你的外卖</h2><h2 ng-if=!order.is_online_paid>订单已成功提交，请耐心等待你的外卖</h2><span class=color-weak>送货至： <em ng-bind=address.name></em> <em ng-bind="address.phone | mobileMask"></em> <em class=pay-header-address ng-bind=address.address></em></span><div class=ordersuccess-tip><p>享受完美食后评价订单还能获得积分哦~ 查看<a href=/profile/points hardjump>我的积分</a></p><p>预测送餐时间为<em class=color-stress ng-bind="leadTime | date:\'HH:mm\'"></em>，请保持手机畅通</p></div><div class=ordersuccess-action><a class="btn-primary btn-lg" hardjump ng-href=/profile/order/id/{{order.unique_id}}>订单详情</a> <a class=inherit hardjump href=/profile/order>我的订单</a></div></div><div class=ordersuccess-aside><img src='+a(117)+' alt=下载饿了么APP><p class=color-mute>使用手机APP下单，优惠更多</p></div></div><div class="ordersuccess-dp container"><div class=ordersuccess-dptitle>附近热门团购</div><iframe class=ordersuccess-frame ng-src={{frameURL}}></iframe></div>'
为何不用单独的文件,而是把代码这样注入
- 另外,在文件中
https://static11.elemecdn.com/eleme/desktop/vendor.7a76a5.js
出现大量的\n简直亮瞎
- 代码的最后部分压缩,部分不压缩,是为了调试方便?还是懒得统一?
- 在https://www.ele.me/place/wtw27pnxv422
<script src="//v2.live800.com/live800/chatClient/textStatic.js"></script>
出现了两次,不是bug?
- 题目中说了不许用别的框架,那么我就不加material design和three.js了
