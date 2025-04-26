# strategy-RandomBuy-StopWin
随机买卖期货策略

博弈项目：技巧概率论（老虎机/股票/期货 vs 网球/足球/围棋）

盈利原因：开仓逻辑占比30%，70%利润奔跑+趋势行情

你敢相信吗？随便抛个硬币也可以实现稳定盈利

文华期货源码 股指期货 15分钟

https://wt8.wenhua.com.cn/#/download/download/1

策略1.随机买卖 
R: RAND(1,2);  // 随机变量R返回1或者2

DAYBARPOS=1 && R=1, BK;  // 每天开盘第一根K线随机变量为1就做多
DAYBARPOS=1 && R=2, SK;  // 每天开盘第一根K线随机变量为2就做空

CLOSE < BKPRICE * (1 - 1/100) || CLOSE > BKPRICE * (1 + 1/100), SP;  // 多单价格上下波动1%平仓
CLOSE > SKPRICE * (1 + 1/100) || CLOSE < SKPRICE * (1 - 1/100), BP;  // 空单价格上下波动1%平仓

AUTOFILTER;                   // 一开一平过滤
TRADE_OTHER('AUTO');          // 自动切换主力合约


策略2.随机买卖 + 动态止盈 
R: RAND(1, 2);  // 随机变量R返回1或者2

DAYBARPOS=1 && R=1, BK;       // 每天开盘第一根K线随机变量为1就做多
DAYBARPOS=1 && R=2, SK;       // 每天开盘第一根K线随机变量为2就做空

CLOSE < BKPRICE * (1 - 1/100) || CLOSE > BKPRICE * (1 + 1/100), SP;  // 多单价格上下波动1%平仓
CLOSE > SKPRICE * (1 + 1/100) || CLOSE < SKPRICE * (1 - 1/100), BP;  // 空单价格上下波动1%平仓

AUTOFILTER;                 // 一开一平过滤
TRADE_OTHER('AUTO');        // 自动切换主力合约

![IMG_9667](https://github.com/user-attachments/assets/7f005f03-b00b-4f25-9afa-3d897f4e1c80)

![IMG_9668](https://github.com/user-attachments/assets/0f78a136-704f-4c6f-9173-c290b7f3a908)

![IMG_9670](https://github.com/user-attachments/assets/8fbe4a51-3faf-4b90-9b8a-dff409a945b2)

![IMG_9672](https://github.com/user-attachments/assets/3adb9dfc-58fe-4935-b4dc-7e829a01b74c)

![IMG_9673](https://github.com/user-attachments/assets/2afab977-7ed8-4061-ba16-cb8c28fba82b)
