# pagination
这是一个基于jQuery的翻页按钮插件！
# 插件调用示例
## HTML代码
    <div class="pagination"></div>
## jQuery代码
	$('.pagination').pagination({
		total: 20,
		current: 5,
		callback: function(e) {
			//参数e为返回的当前页数
			//可以在下面调用e
			console.log(e);
		}
	});
## 完整示例
	<!DOCTYPE html>
	<html>
	<head>
		<meta charset="utf-8">
		<title>分页按钮</title>
		<link rel="stylesheet" type="text/css" href="css/pagination.css">
		<script type="text/javascript" src="js/jquery-1.12.4.min.js"></script>
		<script type="text/javascript" src="js/pagination.js"></script>
		<style type="text/css">
			.box,.show{
				margin: 0 auto;
				padding-top: 256px;
				margin: 10px auto;
				text-align: center;
			}
			.show{
				padding: 0;
			}
		</style>
	</head>
	<body>
		<div class="box">
		    <div class="pagination"></div>
		</div>
		<div class="show"></div>
		<script type="text/javascript">
		$('.pagination').pagination({
		    total: 20,
		    current: 5,
		    callback: function(e) {
		        $('.show').text('当前为：第'+e+'页');
		    }
		});
		</script>
	</body>
	</html>