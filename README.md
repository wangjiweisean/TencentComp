# TencentComp
腾讯T派算法大赛
info: http://algo.tpai.qq.com/home/information/index.html

若字段取值为0或空字符串均代表未知。

### ad.csv  (6582 rows × 6 columns) 
    * no missing values
    creativeID      （6582)  all different
    adID             (3616)
    campaignID       (720)
    advertiserID     (91)
    appID            (50)
    appPlatform      (2)
    No missing value for all 6 variables


### app_categories.csv (217041 rows × 2 columes)
    appID           no missing values
    appCategory     67757 zeros (App开发者设定的App类目标签，类目标签有两层，使用3位数字编码，百位数表示一级类目，十位个位数表示二级类目，如“210”表示一级类目编号为2，二级类目编号为10，类目未知或者无法获取时，标记为0。)

### position.csv (7645 rows × 3 columns)
    positionID      no missing values
    sitesetID       3 uniques , 7556 zeros
    positionType    6 uniques, 92 zeros

### user.csv  ( 2805118 rows × 8 columns)
    userID          all unique
    age             294271 missing value  (取值范围[0, 80]，其中0表示未知。)
    gender          3 uniques, 285098 zeros（取值包括男，女，未知。）
    education       8 uniques,692957 zeros
                                    （小学，初中，高中，专科，本科，硕士，博士，未知）
    marriageStatus  4 uniques, 1130463 zeros（单身，新婚，已婚，未知）
    haveBaby        7 uniques, 2269785 zeros
                                    （孕育中，宝宝0~6个月，宝宝6~12个月，宝宝1~2岁，宝宝2~3岁，育儿但宝宝年龄未知，未知）
    hometown        365 uniques, 958722 zeros
                                    （用户出生地，取值具体到市级城市，使用二级编码，千位百位数表示省份，十位个位数表示省内城市，如1806表示省份编号为18，城市编号是省内的6号，编号0表示未知。）
    residence       400 uniques, 226812 zeros （同 hometown 规则一样）

### user_app_actions.csv ( 6003471 rows × 3 columns) 
    * 训练数据开始时间之前16天开始连续30天的操作流水，即第1天0点到第31天0点
    userID          781112 uniques 
    installTime     6位数字 格式均为DDHHMM，其中DD代表第几天，HH代表小时，MM代表分钟
    appID           100923 uniques



### train.csv 
    label               **responsor
    clickTime           6位数字 格式均为DDHHMM，其中DD代表第几天，HH代表小时，MM代表分钟
    conversionTime      6位数字 格式均为DDHHMM，其中DD代表第几天，HH代表小时，MM代表分钟
    creativeID          see ad.csv
    userID              see user.csv
    positionID          see position.csv
    connectionType      移动设备当前使用的联网方式，取值包括2G，3G，4G，WIFI，未知
    telecomsOperator    移动设备当前使用的运营商，取值包括中国移动，中国联通，中国电信，未知



