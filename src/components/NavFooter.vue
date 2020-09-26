<template>
	<div class="footer">
		<div class="footer-logo">
			<img src="/imgs/logo-footer.png" alt="">
			<p>小米商城</p>
		</div>
		<div class="footer-link">
			<a href="javascript:;">小米商城</a><span>|</span>
			<a href="javascript:;"> MIUI</a><span>|</span>
			<a href="javascript:;">米家</a><span>|</span>
			<a href="javascript:;">米聊</a>
		</div>
		<div class="copyright">
			Copyright ©2019 <span class="domain">mi.com</span> 
	 		All Rights Reserved
	    </div>
	</div>		
</template>
<script >
	export default{
		name:"nav-footer"
	}
</script>

<style lang="scss">
	.footer{
		height:234px;
		border-top:4px solid #ff6600;
		background-color:#333333;
		color:#999999;
		font-size:16px;
		text-align:center;
		.footer-logo{
			margin-top:46px;
			margin-bottom:31px;
		}
		img{
			width:53px;
			height:36px;
			margin-bottom:13px;
		}
		.footer-link{
			a{
			//a标签必须单独设置颜色因为a的优先级大于父类的优先级。	
			display:inline-block;
			color:#999999;
			}
			span{
				margin:0 10px;
			}
			margin-bottom:13px
		}
		.copyright{
			.domain{
				color:#ff6600;
			}
		}
	}
</style>