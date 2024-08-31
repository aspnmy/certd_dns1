<!--
 * @Author: aspnmy support@e2bank.cn
 * @Date: 2024-08-30 06:03:32
 * @LastEditors: aspnmy support@e2bank.cn
 * @LastEditTime: 2024-08-30 11:44:57
 * @FilePath: \docker-hube:\github\certd_dns1\README.md

 -->
# ![certd_dns1](https://avatars.githubusercontent.com/u/7374416?v=4&size=64) certd_dns1 说明

基于开源项目 https://github.com/certd/certd 二开 ，主要修改支持dns1的注册形式，目的是为了实现非自动化注册证书（方便销售ssl证书给客户）。
- 1、使用说明，首先切换模板到new_blue_dns1
- 2、选择注册模式选择dns1，不要选http1，提交注册信息后，会生成dns-txt记录，交给客户让客户自己配置即可。
- 3、验证授权成功后，等待CA授权商颁发证书。
- 4、颁发成功后，点击下载，即可交付给客户。
- 5、如果已经配置了邮件服务器的情况下，可以填写客户的邮箱地址，已发送邮件的形式进行发送。
- 6、版本说明：
- certd_dns1_free 版: https://github.com/aspnmy/certd_dns1_free.git
- certd_dns1_pro 版: https://git.t2be.cn/podAdmin/certd_dns1_pro.git
- 7、支持的授权商：
- certd_dns1_free 支持 https://github.com/certd/certd 项目中自带的3个服务商的dns1模式。
- certd_dns1_pro 支持 14家服务商。
- certd_dns1_pro_cli certd_dns1_pro 集成脚本，主要用于集成以后实现自动化注册，续期。
<!--
 * @Author: aspnmy support@e2bank.cn
 * @Date: 2024-08-30 06:03:32
 * @LastEditors: aspnmy support@e2bank.cn
 * @LastEditTime: 2024-08-30 11:44:57
 * @FilePath: \docker-hube:\github\certd_dns1_pro\README.md

 -->
# certd_dns1_pro 商业版说明
## 独立模式
+ 登陆管理员后台，启动独立模式，只可以管理员登陆，选择dns1注册通道，输入客户要申请的域名，单个或多个或通配符，点击预申请，生成txt验证记录，然后交给客户再自己的dns域中设置txt验证值，等待5-10分钟验证通过，即可签发证书，下载以后可以交付给客户。
## 代理模式
+ 登陆管理员后台，启动代理模式，就可以新增代理用户账户，代理用户为管理员下级子管理员，管理员首先配置子用户的业务权限。子管理员登陆以后，可以根据自己已经有的权限，进行注册证书流程。
+ 子账户即可交给员工使用，也可以交给外部用户使用，具体运营方向看自己。
## 注册扣点模式
+ 启动代理模式后，总管理员可在后台选择是否启用扣点模式，引入虚拟储值积分，卡密模式，非在线充值。开启该模式后，子账号用户申请证书需要扣自己账户对应的虚拟积分。
+ 卡密销售可对接任何一个第三方或者开源组件，总管理员在卡密池中导入卡密数据即可，核销以后（充值核销）会自动虚拟标注核销标志0->1,非实际删除，方便总管理员对账。



