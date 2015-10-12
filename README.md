# PyAutoTrading
股票交易软件辅助工具

## 简介
只能用于华泰证券独立交易软件(同花顺通用版暂时不支持）。先启动交易软件，然后再运行本程序。第一次使用，需在`系统->快速交易` 选型卡下，把 `委托前是否需要确认`和`委托成功后是否弹出对话框`全选为否，在`交易设置`标签页下， 把`默认买入价格`和`默认卖出价格`设置为`卖五价`和`买五价`，另外按`F6`键,把买卖价格锁定为涨停价和跌停价，尽量以市价成交，目前软件还无法知道是否真的成交，只能知道委托是否成功。如果有疑问，或是建议，可以发邮件联系。邮箱：ronghui.ding@outlook.com，或加入QQ群：486224275。

## 注意事项
* 交易软件[下载地址](http://www.htsc.com.cn/browser/download.html "下载")，选第一个`网上交易系统（专业版Ⅱ）V5.48`,交易程序单独运行，不要嵌在行情软件里 。
* 开发环境是win10 64bit, python3 64bit、pywin32、tushare。 以前是用python 32bit开发的，现在好像python 64bit的也能用。
* winguiauto.py这个文件需一同下载，和PyAutoTrading.py放同一目录。
* 不写时间条件单，默认时间为凌晨1点。如果只想要时间条件单而忽略价格条件单，可以写个始终满足条件的价格。其它地方不写，这行将不做处理。
* 股票数量最好为100的倍数，小于100股的不会交易，大于100、非整数倍的将取整, 比如150股将作为100股。
* 时间为24小时制，形式为 “时：分：秒”， 每项都必须写， 后面的写法是错误的： “13：30” 。

## 版本
* v 0.01 修正了股票价格实时显示问题。
* v 0.02 重构了交易软件接口，目前在最小化状态下也可以下单，下单速度加快，增加委托日志。
* v 0.03 重新布局了控件，修改委托日志控件。修复了少许Bug。
* v 0.04 重新布局了控件，重构了monitor函数。现在一次可以下4个条件单。
* v 0.05 加入时间条件单。
* v 0.06 交易软件接口函数单独放winguiauto文件。
* v 0.07 时间条件单和价格条件单相结合，添加保存和载入功能,存档和主文件在同一目录下，名为stockInfo.dat，是个二进制文件。	
* v 0.08 代码清理，添加了注释。现在可以同时监控5只股票。


-----------------------------------
![image](https://github.com/drongh/PyAutoTrading/raw/master/Logo/setting1.gif)
![image](https://github.com/drongh/PyAutoTrading/raw/master/Logo/setting2.gif)
![image](https://github.com/drongh/PyAutoTrading/raw/master/Logo/setting3.gif)
![image](https://github.com/drongh/PyAutoTrading/raw/master/Logo/trading.gif)