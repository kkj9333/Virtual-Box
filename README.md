# Virtual-Box
## minecraft BE bds端插件-玩家多背包系统-虚拟箱子
- **这是一个正在开发的bds端插件**
- 相当于玩家多背包扩展
- 可以以大箱子形式打开一个虚拟的背包，可以自由在虚拟箱子和自己背包之间移动，拿出物品
### 计划实现功能有：
- 支持扩展虚拟背包（需要花费），支持翻页；
- 支持简单的自定义虚拟背包扩展花费计算公式；
- 支持op管理查其他人的虚拟背包；
### 可能加入功能：
- 虚拟背包自动整理，排序**

### DEMO版本🎁
 demo版本意味着不是正式版本，功能并未完善且具有实验性，此页面在正式完成前均处于DEMO版本测试状态。
![virboxDEMO版本操作界面](https://user-images.githubusercontent.com/51207072/185733431-2ed6d0a6-cb8c-44fa-bf74-faa3ca226791.png)
### 如何安装和开始
- 本插件依赖于LiteloaderBDS启动器（2.5.1以上），下载插件后，请将插件丢入plugins目录，运行正常，进入游戏后使用指令/virbox即可开始操作。
### 关于DEMO版本的简要说明
- DEMO版本实现了简单的物品取出，放入，移动操作，实现了翻页和自定义虚拟背包扩展花费计算公式（四则运算）
- OP可以管理他人的虚拟背包，/virbox playername.
 <br/>但有些需要注意的细节：<br>
- 首先，物品交换是不被允许的，物品丢出，合并操作也不被允许，在windows下，虚拟virbox的合并操作会直接成为“交换鼠标选中物品”；
- 游戏中很多原版操作尚未实现，你操作可能会收到插件的警告；如果插件弹出Error（不是Liteloader的），也不用太担心，一般是自动处理的，如果你认为是错误，**请在issue中提交错误说明及复现步骤**。


### 配置文件📋
```javascript
{
    "maxpage": 3,//玩家最大可解锁页数
    "moneymode": 1,//经济运行模式，1=llmoney，0=scoreboard
    "pagecost": 0,//页花费，自定义变量，并非最终花费。
    "paycalculationformula": "{pagecost}+{page}*{page}*2000",//解锁下一页需要花费金钱的计算公式，支持四则运算，如果公式错误会导致异常甚至崩服
    /*公式举例说明
    如果配置项pagecost=0,当前玩家已解锁页数page=1，
    那么解锁下一页需要金钱：0+1*1*2000=2000
    */
    "scoremoneyname": "money" //计分板经济对接的计分板项目名称
}
```
### 关于正式版

- 正式版发布待定，秋季作者有很多事情忙，
- 但收藏超过50，应该会尽快继续完成这部分的工作。



