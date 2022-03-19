# WhetherTheFinancialCreditIsInDefault
# 基于随机森林与逻辑回归的金融贷款违约预测
# 一、项目背景
在当今的金融行业，尤其是在银行等金融机构中，往往允许客户向机构提出借贷等金融流通行为，而对于这些金融机构来说，合理、准确地预测客户是否会违约对于机构的经济保障有重要作用。本次实验通过使用阿里云天池的“0基础入门系列赛事第四场的——零基础入门金融风控-贷款违约预测” 比赛数据集中的数据，建立适当的模型来对新客户样本时候违约进行预测评估。
# 二、数据集说明
本次实验中所使用到的数据集来源于和鲸社区的“金融风控之贷款违约预测数据集”，而该数据集引用的是与阿里云天池联合发起的0基础入门系列赛事第四场的——零基础入门金融风控-贷款违约预测的数据集。
该数据集来自某信贷平台的贷款记录，总数据量超过120万，包含47列变量信息，其中15列为匿名变量。该比赛中使用80万条数据作为训练集，20万条作为比赛测试集，同时对employmentTitle、purpose、postCode和title等信息进行了脱敏，以下表格对不同字段进行了解释。

|属性	|解释	|属性|	解释|
|:---|:---|:---|:---|
id	|为贷款清单分配的唯一信用证标识|	dti	|债务收入比
loanAmnt	|贷款金额|	delinquency_2years|	借款人过去2年信用档案中逾期30天以上的违约事件数
term	|贷款期限（year）|	ficoRangeLow|	借款人在贷款发放时的fico所属的下限范围
interestRate|	贷款利率|	ficoRangeHigh	|借款人在贷款发放时的fico所属的上限范围
installment|	分期付款金额	|openAcc|	借款人信用档案中未结信用额度的数量
grade	|贷款等级	|pubRec|	贬损公共记录的数量
subGrade|	贷款等级之子级|	pubRecBankruptcies	|公开记录清除的数量
employmentTitle|	就业职称	|revolBal	|信贷周转余额合计
employmentLength	|就业年限（年）|	revolUtil	|循环额度利用率，或借款人使用的相对于所有可用循环信贷的信贷金额
homeOwnership	|借款人在登记时提供的房屋所有权状况	|totalAcc	|借款人信用档案中当前的信用额度总数
annualIncome|	年收入|	initialListStatus|	贷款的初始列表状态
verificationStatus	|验证状态	|applicationType|	表明贷款是个人申请还是与两个共同借款人的联合申请
issueDate|	贷款发放的月份	earliesCreditLine|	借款人最早报告的信用额度开立的月份
isDefault |	样本标签	|Title	|借款人提供的贷款名称
purpose	|借款人在贷款申请时的贷款用途类别	|policyCode	|公开可用的策略代码=1新产品不公开可用的策略代码=2
postCode	|借款人在贷款申请中提供的邮政编码的前3位数字|	n0~n14	|匿名特征n0~n14
regionCode	|地区编码		||
# 三、实验目的
使用Python数据分析的相关技术和机器学习的相关算法，针对“阿里云天池0基础入门系列赛事第四场的——零基础入门金融风控-贷款违约预测”比赛赛题进行建模，主要使用随机森林和逻辑回归两个算法进行调参实现，然后运用集成学习的思想使用排序平均法、Boosting法等进行模型融合，最终获得最佳的模型。
# 四、实验环境
操作系统：Windows 10

编译器：Jupyter Notebook 6.3.0

Python：3.8.8

CPU：intell 10th i7、intell 11st i7

显卡：NVIDIA GeForce RTX 1650、NVIDIA GeForce RTX 3070

其他模块：sklearn、scipy、numpy、scikitplot、missingno、random、joypy、math、warnings、operator、pandas、gc、tqdm、seaborn等
# 五、实验流程设计
该实验的具体的流程设计如以下思维导图所示：
![image](https://user-images.githubusercontent.com/68093996/159116614-62c73f40-73e3-4dc6-9bfa-bc2c4d33d1c2.png)

