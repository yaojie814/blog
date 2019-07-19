这个是about-关于我中的打赏功能.

在md文件中添加以下代码即可：

<link rel="stylesheet" type="text/css" href="/images/pay/pay.css" />
<div class="content"><p><a href="javascript:void(0)" onclick="dashangToggle()" class="dashang" style="padding:10px;color:#fff;text-decoration:none;" title="打赏，支持一下">打赏</a></p><div class="hide_box"></div><div class="shang_box"><a class="shang_close" href="javascript:void(0)" onclick="dashangToggle()" title="关闭"><b style="font-size:20px;">×</b></a><div class="shang_tit"><p style="font-weight:600;">感谢您的支持，我会继续努力的!</p></div><div class="shang_payimg"><img style="padding:0;" src="/images/pay/alipayimg.jpg" title="扫一扫" /></div><div class="pay_explain">扫码打赏，你说多少就多少</div><div class="shang_payselect"><div style="width:115px;height:32px;" class="pay_item checked" data-id="alipay"><span class="radiobox"></span><span class="pay_logo"><div style="background:url('/images/pay/alipay.jpg');margin-left:30px;height:28px;width:85px;"></div></span></div><div   style="width:142px;height:32px;" class="pay_item" data-id="weipay"><span class="radiobox"></span><span class="pay_logo"><div style="background:url('/images/pay/wechat.jpg');margin-left:30px;height:28px;width:112px;"></div></span></div></div><div class="shang_info"><p style="font-weight:600;">打开<span id="shang_pay_txt">支付宝</span>扫一扫，即可进行扫码打赏哦</p></div></div><img src="/images/pay/weipayimg.jpg" style="display:none;"/></div>

<script type="text/javascript">
$(function(){
	$(".pay_item").click(function(){
		$(this).addClass('checked').siblings('.pay_item').removeClass('checked');
		var dataid=$(this).attr('data-id');
		$(".shang_payimg img").attr("src","/images/pay/"+dataid+"img.jpg");
		$(".shang_payimg a").attr("href","/images/pay/"+dataid+"img.jpg");
		$("#shang_pay_txt").text(dataid=="alipay"?"支付宝":"微信");
	});
});
function dashangToggle(){
	$(".hide_box").fadeToggle();
	$(".shang_box").fadeToggle();
}
</script>