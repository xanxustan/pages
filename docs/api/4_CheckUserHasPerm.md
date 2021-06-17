---
sort: 4
---

# 判断用户是否有权限

## 基本信息

**Path：** /api/v1/CheckUserHasPerm

**Method：** POST

**接口描述：**


## 请求参数

**Headers**

| 参数名称          | 参数值              | 是否必须 | 示例 | 备注 |
|---------------|------------------|------|----|----|
| Content-Type  | application/json | 是    |    |    |
| Authorization | token            | 是    |    |    |

**Body**

| 名称       | 类型      | 是否必须 | 默认值 | 备注   | 其他信息 |
|----------|---------|------|-----|------|------|
| gid      | integer | 必须   |     | 群组ID |      |
| uid      | integer | 必须   |     | 用户ID |      |
| perms_id | integer | 必须   |     | 权限ID |      |

**权限列表**

| 权限ID | 权限名称    | 说明                   |
|------|---------|----------------------|
| 4000 | 管理机器人配置 | 拥有此权限的成员可以修改群组Bot设置。 |

## 返回数据

| 名称  | 类型      | 是否必须 | 默认值 | 备注                   | 其他信息 |
|-----|---------|------|-----|----------------------|------|
| ret | integer | 必须   | 0   |                      |      |
| msg | string  | 必须   | ok  |                      |      |
| has | bool    | 必须   |     | true-有权限 false-无权限 |      |