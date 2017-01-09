# TaoYinApi

This file file serves as your book's preface, a great place to describe your book's content and ideas.

##一：通用类
###1:短信发送（POST）
https://localhost:8080/taoyinShop/ty/sms/send
```js
param:{
    "mobile": "13422222222",                 //手机号  必填
    "type": "01"                             //类型 01：通用 02：其他  非必填 默认01
    "access_token": "fsfGhsdSdTv24354bg",    //未登录前发送该token
    }
```
```js
response:{
    "data": null
    "message": "发送成功", 
    "status": true
    }
```
##二：用户类
###1:会员注册（POST）
https://localhost:8080/taoyinShop/ty/member/memberRegist
```js
param:{
     "username": "13422222222", //手机号  必填
     "password": "sad1531" //密码  必填
     "authCode": "151545", //验证码  必填
     "registerCode": "dsad4dsa2dsad151dasd" //邀请码  非必填
     "access_token": "fsfGhsdSdTv24354bg",未登录前发送该token
     }
```
```js
response:{
    "data": {
            "id": “dsa4d6adsa4dsa5dad151dsa5sawefg5”, 
            "username": "13422222222", 
            "password": "dcsasadsadsadsaccvh16515153", 
            "salt": "s4s5sa1dsadsadsa1c15d1sd1a6", 
            "registerCode": "d149b21032b1f439a900a5d1c90447b2"
            "code": "d149b21032b1f439a900a5d1c90447b2"
            "status": “Y”, //状态  启用禁用
            "busMark": "Y", //商家标志 
            "busStatus": "Y"
            "creatTime": “1992-02-05 12:12:12”
            "editTime": "1992-02-05 12:12:12", 
            }, 
        "message": "注册成功", 
        "status": true
    }
```
###2:会员登录（POST）
https://localhost:8080/taoyinShop/ty/member/memberLogin
```js
param:{
    "username": "13422222222", //手机号  必填
    "password": "sad1531" //密码  必填
    "access_token": "fsfGhsdSdTv24354bg",  未登录前发送该token
    "udid ": "xxx",  设备唯一标识
    }
```
```js
response:{
"data": {
        "id": “dsa4d6adsa4dsa5dad151dsa5sawefg5”, 
        "username": "13422222222", 
        "password": "dcsasadsadsadsaccvh16515153", 
        "salt": "s4s5sa1dsadsadsa1c15d1sd1a6", 
        "registerCode": "d149b21032b1f439a900a5d1c90447b2"
        "code": "d149b21032b1f439a900a5d1c90447b2"
        "status": “Y”, //状态  启用禁用
        "busMark": "Y", //商家标志 
        "busStatus": "Y"
        "creatTime": “1992-02-05 12:12:12”
        "editTime": "1992-02-05 12:12:12", 
        "access_token": "xxx",  接口调用标识
        }, 
     "message": "登录成功", 
     "status": true
     }
```

###3:个人资料（POST）
https://localhost:8080/taoyinShop/ty/member/memberDetails

```js
param:{
    "memId": "dfsssdff", //会员id  必填
    "access_token": "fsfGhsdSdTv24354bg",  登录后获取的token
    }
```
```js
response:{
     "data": {
        "id": “dsa4d6adsa4dsa5dad151dsa5sawefg5”, 
        "username": "13422222222", 
        "registerCode": "d149b21032b1f439a900a5d1c90447b2"
        "code": "d149b21032b1f439a900a5d1c90447b2"
        "busMark": "Y", //商家标志 
        "photo": "/img/ss.jpg"  //头像
        "nickname": "xxx"  //会员昵称
        "realname": "xxx"  //真实姓名  为空则未实名认证
        "sex": "0" // 0：女1：男
        }, 
    "message": "成功", 
    "status": true
}
```

###4.修改个人密码（POST）
https://localhost:8080/taoyinShop/ty/member/memberpwUpdate
```js
param:{
    "memId": "dfsssdff", //会员id  必填
    "access_token": "fsfGhsdSdTv24354bg",  登录后获取的token
    "oldpassword": "dfsssdff", //原密码  必填
    "password": "xdsd",  //新密码 必填
}
```
```js
param:{
    "data": null
    "message": "密码修改成功", 
    "status": true
    }
```

###5:修改个人详细信息（POST）
https://localhost:8080/taoyinShop/ty/member/memberDetailsUpdate
```js
param:{
    "memId": "dfsssdff", //会员id  必填
    "access_token": "fsfGhsdSdTv24354bg",  登录后获取的token
    "photo": "xxx", //头像  选填
    "nickname": "xxx",  /昵称  选填
    "sex": "0",  /性别  选填  0：女 1：男
    }
```
```js
response:{
    "data": null
    "message": "修改成功", 
    "status": true
    }
```