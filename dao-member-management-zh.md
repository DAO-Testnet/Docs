# aelf DAO管理委员会成员加入/退出操作指南

英文版教程链接：[dao-member-management](https://github.com/DAO-Testnet/Docs/blob/master/dao-member-management.md)

---

## 1.aelf DAO管理委员会成员加入
### 1.1 aelf DAO管理委员会加入条件
抵押一定数量的ELF（具体数量待aelf DAO管理委会员决议确定）

### 1.2 aelf DAO管理委员会加入流程
![图片](https://uploader.shimo.im/f/qT32N1zFgZ5PBAwa.png!thumbnail)

### 1.3 aelf DAO管理委员会加入指南
**1.3.1 申请提案：**

* 申请人进入[浏览器-提案](https://explorer-test.aelf.io/proposal?#https%3A%2F%2Fexplorer-test.aelf.io%2Fviewer%2Fproposal.html%3Frandom%3D7b08e671%23%2Fapply)页面，申请议会模型（Parliament）提案，选择/输入以下内容：

![图片](https://uploader.shimo.im/f/mj7GU0GI1Pw6iino.png!thumbnail)

图1.1-申请提案

* Proposal Mode：Parliament
* Organization：生产节点组织
* Contract Address：aelf DAO合约地址
* Method Name：ProposeJoin
* Method Params：发起人自己的地址
* Expiration Time：选择合适的时间，需保证不影响项目开发，且组织成员有足够的时间投票（建议：7天以内）

**1.3.2 提案投票：**

申请成功的项目提案将在提案公示页面展示，生产节点组织对该提案进行投票（同意/反对/弃权）；

![图片](https://uploader.shimo.im/f/0DxzhY7reFwu5dtV.png!thumbnail)

图1.2-投票

**1.3.3 提案执行：**

* 如果投票通过，需由申请人在到期前执行提案；执行成功即该申请人加入成功；同时链上对抵押的ELF进行锁仓；
* 如果投票未通过，将退还抵押的ELF。
### 1.4 加入成功后aelf DAO管理委员会的组织变更
aelf DAO管理委员会成员加入后，aelf DAO合约会自动调整aelf DAO管理委员会组织成员和投票阈值；即aelf DAO管理委员会成员有变更时，这些数据都会被自动设置为当前aelf DAO管理委员会成员数量的1/2。

**aelf DAO****管理委员会****组织要求和权限：**

**创建人：** aelf DAO合约

**组织阈值修改权限：** aelf DAO管理委员会组织初始成员

**组织内容：**

| 模型 | 协会合约模型Association Contract | 
|:----|:----|
| 组织成员   | aelf DAO管理委员会成员 (aelf DAO合约部署后，初始化时可以传入aelf DAO管理委员会初始成员，如果没有初始成员，则这条链的节点为初始成员)   | 
| 提案白名单   | aelf DAO合约   | 
| 提案通过阈值   | 同意>=1，反对<=0，弃权<=0，总票数>=1  （对于aelf DAO管理委员会成员投票的实际阈值：同意>=50%，反对<=50%，弃权<=50%，总票数>=50%，该阈值在修改时需输入数值，以比例换算对应数值）   | 

---

## 2.aelf DAO管理委员会成员退出
### 2.1 aelf DAO管理委员会退出流程
主动退出：成员随时可以退出，退出需要发起提案，提案通过即退出成功，用户执行提案后，自动退还抵押的ELF；

被动退出：有恶意行为的成员会由其它成员发起提案强制退出，并没收/销毁 token。

![图片](https://uploader.shimo.im/f/2Qf0TUgyL5AWprbV.png!thumbnail)

### 2.2 aelf DAO管理委员会退出指南
**2.2.1 申请提案：**

申请人进入[浏览器-提案](https://explorer-test.aelf.io/proposal?#https%3A%2F%2Fexplorer-test.aelf.io%2Fviewer%2Fproposal.html%3Frandom%3D7b08e671%23%2Fapply)页面，申请议会模型（Parliament）提案，选择/输入以下内容：

![图片](https://uploader.shimo.im/f/qLWt2gUk4Ugo6ZVH.png!thumbnail)

图2.1-申请提案

* Proposal Mode：Parliament
* Organization：生产节点组织
* Contract Address：aelf DAO合约地址
* Method Name：ProposeQuit（主动退出）、ProposeExpel（被动退出）
* Method Params：退出的成员地址（主动退出）、试图开除的成员地址（被动退出）
* Expiration Time：选择合适的时间，需保证不影响项目开发，且组织成员有足够的时间投票（建议：7天以内）

**2.2.2 提案投票：**

申请成功的项目提案将在提案公示页面展示，生产节点组织对该提案进行投票（同意/反对/弃权）；

![图片](https://uploader.shimo.im/f/0DxzhY7reFwu5dtV.png!thumbnail)

图2.2-投票

**2.2.3 提案执行：**

* 如果投票通过后，由申请人在到期前执行提案；提案执行成功后即该申请人退出成功；同时链上对抵押的ELF进行退还或没收/销毁；
* 如果投票未通过，成员退出失败。

### 2.3 退出成功后aelf DAO管理委员会的组织变更
aelf DAO管理委员会成员加入后，aelf DAO合约会自动调整aelf DAO管理委员会组织成员和投票阈值；即aelf DAO管理委员会成员有变更时，这些数据都会被自动设置为当前aelf DAO管理委员会成员数量的1/2。

---

## 3.我们的社区
### GitHub Organization
GitHub Organization用于投资项目的申请、赏金项目的发布、项目进度跟进、开发成果提交等，在GitHub Organization可以看到DAO社区所有项目的开发情况；社区用户可通过以下链接进入aelf DAO GitHub Organization：

aelf DAO Testnet: [https://github.com/DAO-Testnet](https://github.com/DAO-Testnet)

1. GitHub“投资项目”仓库：[https://github.com/DAO-Testnet/Grants](https://github.com/DAO-Testnet/Grants)
2. GitHub“赏金项目”仓库：[https://github.com/DAO-Testnet/Bounties](https://github.com/DAO-Testnet/Bounties)
3. GitHub”DAO文档“仓库：[https://github.com/DAO-Testnet/Docs](https://github.com/DAO-Testnet/Docs)

### Telegram社群
aelf全新的去中心化自治社区：saelf governed community Telegram社群

通过saelf governed community Telegram社群，用户可以更便捷、更及时深度参与到aelf DAO的管理制度建立与发展事项当中，同时根据其参与及贡献程度，可获得相应权益，共同分享aelf的发展成果。社群成员可在群内参与aelf DAO管理制度草案的讨论与决策，并有资格申请加入aelf DAO管理委员会。saelf governed community Telegram社群采用官方邀请加入的方式，详细规则请见：[加入saelf governed community Telegram社群](https://mp.weixin.qq.com/s/kCuMGk2IPiQQHeF9w_YSFQ)

