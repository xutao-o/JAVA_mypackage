# SetPo_XT 自动生成PO文件
SetPo_XT能通过数据库连接生成每张表的po文件，自动处理数据类型并附加注释
### 使用教程
1.下载当前文件jar在package >>> SetPo_XT.jar

2.在项目中引入SetPo_XT.jar

3.调用FoundPo()



     Connection conas = null;
		try {
			Class.forName("com.mysql.jdbc.Driver");
			conas = DriverManager.getConnection("jdbc:mysql://localhost:3306/demo","root","root");
		} catch (SQLException | ClassNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} 
		SetPo_XT.FoundPo(conas,"com.po");
	
### SetPo_XT.FoundPo(conas,"com.po");
第一个参数为连接数据库后的Connection，第二参数为包名创建的po文件会在指定包名下

码云地址：https://gitee.com/qiuqiu_XT/JAVA/tree/master
