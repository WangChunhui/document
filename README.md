# document

	README.md 	: 编辑工作任务、内容， 记录工作进度
	bug.txt		：记录项目bug
	workconfig	：记录工作规则


工作日志

2018.03.27

	-- 整理桌面文档
	-- 根目录下无用文件统一放到一个文件夹里边 file
	-- 查看交接文档
	-- 查看itunes账户信息以及公司apps线上信息
	-- 查看接收测试账号信息
	-- 查看公司app（十年）代码
	eg 
	---- 线上项目两个 《赢家视频录制》《赢家》
	---- 赢家视频录制 未测试
	---- 赢家 未完全测试

2018.03.28

	-- 整理交接文档放到git目录
	-- 查看项目代码
	-- copy项目代码到git

	eg
	----项目网络请求使用afn
	----加密方式 wanglei+时间(yyyy-MM-dd)+c#M8y^8C$UJ%p&75@!   MD5
	----本地化用户信息 （沙盒）


2018.03.29

	-- 开展工作
	eg:
	----调试接口
	----调试查看日志
	----调试token生成

	

2018.03.30

	-- 工作计划
	eg：
	----修改高级体系课程界面以及数据

	讲师课程分开HIGH & HIGH2
	并添加子界面
	子界面数据分页
	

2018.4.2

	-- 工作任务
	eg： 
	----将高级体系课程从公用体系中分离出来 上拉加载功能待完善
	----添加高级体系课程跟多界面 待完善（40%）



2018.4.8

	-- 工作任务

	eg：
	----完成高级体系课程体系
	1. 添加高级体系课程列表界面
	2. 修改高级体系课程更多界面
	3. 修改课程名称展示
	4. 添加课程讲师 课程标签
	----完成费用界面修改 和 部分数据封装
	1. 修改vip直播界面 （点击更多展开）
	2. 修改vip高级体系课程界面 （重构cell）
	3. 创建vip高级体系课程 数据model 
	4. 创建获取体系课程名称api 
	----修改确认订单界面 课程名称
	1. 添加体系课程 课程名称标签 <体系课（第一套）知行合一 投资赢家>
	


2018.4.13

	-- 工作任务
	eg:
	----优化推广界面
	1. 获取不到数据时状态优化
	2. 立刻邀请 和 邀请规则按钮优化
	----查看原码


2018-05-04 工作任务

	1. 修改立即邀请界面 展示文字 /** 已结束 */
	/*
	通过您的邀请，成功注册的新用户数量：
	1.达到1位时，可获得线上课程抵用券4张（价值1800元），有效期30天；
	2.达到7位时，可获得所有讲师VIP直播课程（股票+期货）观看权限一周（价值2980元）；
	3.达到30位时，可获得所有讲师VIP直播课程（股票+期货）观看权限一个月（包含第2条中的7天在内一共30天，价值9800元）
	*/

	2. 修改分享链接 好友界面 描述信息 /** 已结束 */
	title:免费赠送您赢家网所有老师股票、期货VIP课程3天!另!赠送经典投资书籍一本
	description:我一直在赢家网听课，收获颇多，邀您一起共享投资智慧。
	3. 修复邀请卡片信息展示缺失问题(分享出去图片未显示 头像、用户名称、邀请码) /** 已结束 */
	
	网络请未完成 即允许分享
	4. 添加功能 首页推广提示 /** 已结束 */ 
	5. 添加功能 签到 

2018年5月14日

	1. 通知后台修改富文本字段状态
	2. 申请苹果开发者账号续费
	3. 测试更新按钮功能
	4. 重构关于软件界面
	5. 修复bug （线下培训界面 发布状态按钮不显示）




2018年5月15日

	1. 课程表直播间
		接口分析
		{
			"id": "97",
               		"uname": "叶军",
                	"name": "股票",
                	"start_time": "1525741200",
                	"end_time": "1525743000",
                	"playback_url": 5858,
                	"room_id": "12",
                	"type": "0"
		}

		id:课程id
		uname:讲师姓名
		name:课程类型
		start_time:课程开始直播时间
		end_time:课程直播结束时间
		playback_url:回放地址 
		room_id:房间号
		type:是否是公开课


		playback_url
		为空:
			-->当直播时间已过 提示“回放生成中”
			-->直播时间还没到 提示“即将直播”
		不为空：
			-->直播时间已过 提示“观看回放”
			-->直播时间正在进行 提示“直播中”

	2. 课程安排
		接口分析：
		{
        	        "t": 1525622400,// 时间戳
                 	"w": "周一",	// 星期
                	"s": "05月07日"	// 日期
            	}

		t：时间戳 获取某一天的直播视频抛给服务器的字段


	3. 课程安排 直播 和 回放 点击按钮 处理方法需要 区别对待
		直播：传入参数 room_id lid token 到直播控制器
		回看：保持不变


2018-05-16

	1. 修改直播间bannar数据量（15）
	2. 对接打卡功能接口
	3. 封装网络请求接口（WJHttpRequest）
	4. 创建打卡退款功能接口


	5. 全部课程讲师segment接口（是否动态同步 所有讲师）
	6. 创建 请求数据包 param 、api、model


2018-05-17

	1. 打卡记录界面 需要 封装user序列化问题（扩展 而不是 重构）
	2. 处理网络请求成功之后的业务逻辑
	3. 调试界面

2018-05-18

	1. 转移项目到 码云 gitee.com
	2. 公司mac 需要生成ssh key 然后添加到项目中 (便于自己管理项目权限)
	3. 步骤:
		ssh-keygen -t rsa -C "xxxxx@xxxxx.com" 
		cat ~/.ssh/id_rsa.pub
		将公钥添加到项目中
		ssh -T git@git.oschina.net
	4. clone 下来项目 检查 无误 将github中删除
	5. 删除本地 product 和 document 分支

2018-05-19

	1. 打卡活动 申请还款功能实现
	2. 视频播放打卡功能实现（添加接口）
	3. 课程安排表直播数据接口调用？？


2018-05-21

	1. 直播播放器 和 普通播放器不是一个播放器界面 
	2. 添加获取观看时间 需要 区分直播和回看播放
	3. 
