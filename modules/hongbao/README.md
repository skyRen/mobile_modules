
# 生成获取固定个数的红包列表
# 提供 petPacket 模块方法：领红包；
						 >> 按顺序每次领取一个红包
						 >> 返回 number 类型的红包金额，出错返回 -1
						 （出错：1、最小红包金额 * 红包个数 > 总金额；
						 		2、红包已领完 ）
# 以下为引用模块，和初始化参数介绍：

/**
* e.g. 
*
*   // 引入模块，并初始化
*	var HongBao = require('hongbao')({
*			number : 100,    // 红包个数 100个 ，必选
*			total : 50,      // 总金额 50元 ， 必选
*			maxValue : 2,    // 单个红包最大额度 2元，可选，默认1
*			minValue : 0.1,  // 单个红包最小额度 0.1元， 可选，默认0.1
*			repeat : 3       // 2元的红包最多连续出现 3 次， 可选，默认2
*	});
*   
*   // 领红包
*   var package1 = HongBao.getPacket(),
*		package2 = HongBao.getPacket();
*
*/