﻿﻿﻿﻿﻿﻿﻿﻿# 委托UI发送评审说明
## 文档评审
### 链接路径
/ReviewCenter/AddOrEditReview
### 参数
|参数 | 说明 |默认值|
| --- | :-- |:--|
|reviewId |评审ID，新建时此参数不用传  |0
|versionNum|评审版本号，新建时此参数不用传|1
|projectId|项目ID|0
|reviewNodeId|对象ID，多个用逗号分隔|'0'
|nodeName|对象名称，多个对象直接显示为【多个对象】|''
|nodeType|评审对象类型，当按基线中对象类型发送评审时需要传此参数|'0'
|reviewBaseLine|评审对象所在基线ID|'-1'
|reviewName|评审名称|''
|reviewDeadlineDate|评审截止日期，例：2018/10/11|''
|checkList|评审准则，传检查单对象ID，多个用逗号分隔|‘’
|reviewActivityId|评审关联的评审活动ID，需注意评审活动的类型|‘’
|message|评审的描述|‘’
|userList|已选评审用户，数据格式为：[{"UserName":"用户登录名","Approver":true/false是否为审核人,"Reviewer":true/false是否为评审人,"Recorder":true/false是否为记录员,"Engineer":true/false是否为被评人,"QA":true/false是否为QA,"ReviewerLevel":0/1评审人等级},{...},...]|''
|disabledItems|不可修改的属性，可取值为projectId,reviewNodeId,reviewBaseLine,reviewName,reviewDeadlineDate,checkList,reviewActivityId,message,RCheckList,ICheckList,userList|''
|RCheckList|评审检查单，传检查单对象ID，多个用逗号分隔|‘’
|ICheckList|条目检查单，传检查单对象ID，多个用逗号分隔|‘’
|cmUrl|配置项路径，格式为：Rest/CM/project/项目ID/library/配置库类型(DynRepo-开发库、ControlledRepo-受控库、StaticRepo-产品库)/ci/配置项ID/trunk(分支)/具体资源层级目录|‘’
|openReviewWarn|是否开启打开评审弹框，True-开启；False-不开启|‘False’
## 代码评审
### 链接路径
/CodeReview/EditCodeReview
### 参数
|参数 | 说明 |默认值|
| --- | :-- |:--|
|reviewId |评审ID，新建时此参数不用传  |0
|versionNum|评审版本号，新建时此参数不用传|1
|reviewSource|评审资源来源，默认为VISSLM平台，可选值有VISSLM及【代码评审】类型的适配器名称|‘VISSLM’
|reviewItemZip|评审资源是否为压缩包，取值为True/False|'False'
|url|评审资源路径，需与评审来源对应。VISSLM资源路径可参考【配置项路径字段类型】，格式为：(IP+/alm)/Rest/CM/project/项目ID/library/配置库类型(DynRepo-开发库、ControlledRepo-受控库、StaticRepo-产品库)/ci/配置项ID/trunk(分支)/具体资源层级目录。暂不支持svn资源路径|‘’
|projectVersion|评审资源版本|‘’
|fileSuffix|过滤文件后缀名，多个逗号分隔|''
|reviewName|评审名称|''
|reviewDeadlineDate|评审截止日期，例：2018/10/11|''
|checkList|评审准则，传检查单对象ID，多个用逗号分隔|‘’
|reviewActivityId|评审关联的评审活动ID，需注意评审活动的类型|‘’
|message|评审的描述|‘’
|userList|已选评审用户，数据格式为：[{"UserName":"用户登录名","Approver":true/false是否为审核人,"Reviewer":true/false是否为评审人,"Recorder":true/false是否为记录员,"Engineer":true/false是否为被评人,"QA":true/false是否为QA,"ReviewerLevel":0/1评审人等级},{...},...]|''
|disabledItems|不可修改的属性，可取值为reviewSource,reviewItemZip,url,projectVersion,fileSuffix,reviewName,reviewDeadlineDate,checkList,reviewActivityId,message,RCheckList,userList|''
|RCheckList|评审检查单，传检查单对象ID，多个用逗号分隔|‘’
|openReviewWarn|是否开启打开评审弹框，True-开启；False-不开启|‘False’























