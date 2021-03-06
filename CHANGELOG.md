# Changelog

## 2019.04.25

## 新增

- WebLogic wls9-async RCE CNVD-C-2019-48814 by Ntears

## 2019.04.09

## 新增

- Confluence CVE-2019-3396 SSTI to RCE(出于漏洞影响考虑不公开RCE脚本，故仅检测文件读取)

## 2019.03.26

## 修改

- 修复了设置目标文件中url包含'-'无法正常运行的bug

- 修复了目标超多时的卡死问题

- 修改了对不解析域名的处理，使Perun可以直接加载未经有效性验证的域名列表文件

## 新增

- Zimbra CVE-2019-9670 从XXE到RCE Vuln模块(出于漏洞影响考虑不公开RCE脚本，故仅检测XXE)

## 2019.02.24

## 新增

- [Perun/vuln/smb_netbios/new_ms17_010.py](https://github.com/WyAtu/Perun/blob/master/vuln/smb_netbios/new_ms17_010.py)Vuln模块，新的MS17-010检测模块，之前的模块Payload可能会有漏报情况发生

## 2019.02.23

## 新增

- [Perun/vuln/jenkins/unauth2rce.py](https://github.com/WyAtu/Perun/blob/master/vuln/jenkins/unauth2rce.py)Vuln模块，用于检测可能存在的Jenkins pre-auth RCE漏洞

## 2019.01.27

### 新增

- [Perun/vuln/cerio/cerio_auth_rce.py](https://github.com/WyAtu/Perun/blob/master/vuln/cerio/cerio_auth_rce.py)Vuln模块，用于检测CERIO路由器认证后的RCE漏洞(CVE-2018-18852)

- [Perun/vuln/mikrotik/winbox_cve_2018_14847.py](https://github.com/WyAtu/Perun/blob/master/vuln/mikrotik/winbox_cve_2018_14847.py)Vuln模块，用于检测MikroTik RouterOS Winbox未经身份验证的任意文件读/写漏洞(CVE-2018-14847)

## 2019.01.23

### 修改

- [Perun/lib/pingscan.py](https://github.com/WyAtu/Perun/blob/master/lib/pingscan.py)设置目标过多(如10.0.0.0/16、超大目标文件等)时无法进行Ping扫描的问题

- [Perun/lib/requester.py](https://github.com/WyAtu/Perun/blob/master/lib/requester.py)中的Requester类，HTTP请求返回400状态码，导致未抛出异常使程序无法跳至进行HTTPS请求的问题

- [Perun/lib/requester.py](https://github.com/WyAtu/Perun/blob/master/lib/requester.py)中的Requester类，Get方法返回404状态码未捕获页面内容的遗漏

- [Perun/vuln/iis/iis_webdav_put.py](https://github.com/WyAtu/Perun/blob/master/vuln/iis/iis_webdav_put.py)Vuln模块的http应为https的遗漏

### 新增

- [Perun/vuln/jenkins/user_enumeration.py](https://github.com/WyAtu/Perun/blob/master/vuln/jenkins/user_enumeration.py)Vuln模块，用于Jenkins用户名枚举

- [Perun/vuln/iis/short_filename.py](https://github.com/WyAtu/Perun/blob/master/vuln/iis/short_filename.py)Vuln模块，用于检测IIS短文件名漏洞

- [Perun/vuln/mssql/mssql_weakpwd.py](https://github.com/WyAtu/Perun/blob/master/vuln/mssql/mssql_weakpwd.py)Vuln模块，用于检测MSSQL弱口令

- [Perun/vuln/grafana/grafana_weakpwd.py](https://github.com/WyAtu/Perun/blob/master/vuln/grafana/grafana_weakpwd.py)Vuln模块，用于检测Grafana弱口令

- [Perun/vuln/glassfish/glassfish_weakpwd.py](https://github.com/WyAtu/Perun/blob/master/vuln/glassfish/glassfish_weakpwd.py)Vuln模块，用于检测Glassfish弱口令

## 2019.01.16

### 修改

- [Perun/lib/requester.py](https://github.com/WyAtu/Perun/blob/master/lib/requester.py)中的Requester类，使其支持Proxy代理设置，和随机User-Agent头功能

- [Perun/vuln/thinkphp/thinkphp5_rce.py](https://github.com/WyAtu/Perun/blob/master/vuln/thinkphp/thinkphp5_rce.py)Vuln模块的检测方法，避免phpinfo首页错报等情况

- [Perun/vuln/thinkphp/thinkphp5023_rce.py](https://github.com/WyAtu/Perun/blob/master/vuln/thinkphp/thinkphp5023_rce.py)Vuln模块的检测方法，使其兼容不同系统

### 新增

- [Perun/vuln/thinkphp/thinkphp5010_rce.py](https://github.com/WyAtu/Perun/blob/master/vuln/thinkphp/thinkphp5010_rce.py)Vuln模块，用于检测ThinkPHP 5.0.\*(低于5.0.10)远程代码执行漏洞

- [Perun/vuln/thinkphp/thinkphp5152_rce.py](https://github.com/WyAtu/Perun/blob/master/vuln/thinkphp/thinkphp5010_rce.py)Vuln模块，用于检测ThinkPHP 5.1.*/5.2.*(5.1.x - 5.1.31, 5.2.0beta1)远程代码执行漏洞

- [Perun/vuln/nginx/nginx_httproxy.py](https://github.com/WyAtu/Perun/blob/master/vuln/nginx/nginx_httproxy.py)Vuln模块，用于检测Nginx配置不当导致正向代理

## 2019.01.11

### 新增

- [Perun/vuln/thinkphp/thinkphp5_rce.py](https://github.com/WyAtu/Perun/blob/master/vuln/thinkphp/thinkphp5_rce.py)Vuln模块，用于检测ThinkPHP 5.0.\*/5.1.\*远程代码执行漏洞

- [Perun/vuln/thinkphp/thinkphp5023_rce.py](https://github.com/WyAtu/Perun/blob/master/vuln/thinkphp/thinkphp5023_rce.py)Vuln模块，用于检测ThinkPHP5.0.\*(低于5.0.23)远程代码执行漏洞

## 更早

### 无记录
