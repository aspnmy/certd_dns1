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
