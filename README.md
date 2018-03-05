# Nebunaconf
## 去中心化配置中心
创建配置文件  
nebunadb/config.yaml 内容：  
```
[  
   { id: 1,  
     name: dbbackend1  
     host: 10.1.1.2  
    },  
   { id: 2,  
     name: dbbackend2  
     host: 10.1.1.3  
    }  
 ]  
```
## 配置命令
nebuna conf -get nebunadb.config  
nebuna conf -get nebunadb.config "#id=1 and #name like 'dbbackend?'"   
nebuna conf -put nebunadb.config ./config.yaml  
nebuna node -list  
nebuna seednode -list  
nebuna node -add 10.1.2.10  
