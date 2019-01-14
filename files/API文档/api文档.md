# 接口文档

## 目录：
	1). 登陆
	2). 添加用户
	3). 更新用户
	4). 获取所有用户列表
	5). 删除用户
	6). 获取一级或某个二级分类列表
	7). 添加分类
	8). 更新品类名称
	9). 根据分类ID获取分类
	10). 获取商品分页列表
	11). 根据ID/Name搜索产品分页列表
	12). 添加商品
	13). 更新商品
	14). 对商品进行上架/下架处理
	15). 上传图片
	16). 删除图片
	17). 添加角色
	18). 获取角色列表
	19). 更新角色(给角色设置权限)
	20). 获取天气信息(jsonp)

## 1. 登陆

### 请求URL：
	http://localhost:5000/login

### 请求方式：
	POST

### 参数类型

	|参数		|是否必选 |类型     |说明
	|username    |Y       |string   |用户名
	|password    |Y       |string   |密码

### 返回示例：
	成功:
      {
        "status": 0,
        "data": {
          "_id": "5c3b297dea95883f340178b0",
          "password": "21232f297a57a5a743894a0e4a801fc3",
          "username": "admin",
          "create_time": 1547381117891,
          "__v": 0,
          "role": {
            "menus": []
          }
        }
      }
	失败
	  {
        "status": 1,
        "msg": "用户名或密码不正确!"
      }

## 2. 添加用户

### 请求URL：
	http://localhost:5000/manage/user/add

### 请求方式：
	POST

### 参数类型

	|参数		|是否必选 |类型     |说明
	|username    |Y       |string   |用户名
	|password    |Y       |string   |密码
	|phone       |N       |string   |手机号
	|email       |N       |string   |邮箱
	|role_id     |N       |string   |角色ID

### 返回示例：
	成功:
	  {
        "status": 0,
        "user": {
          "_id": "5c3b382c82a14446f4ffb647",
          "username": "admin6",
          "password": "d7b79bb6d6f77e6cbb5df2d0d2478361",
          "phone": "13712341234",
          "email": "test@qq.com",
          "create_time": 1547384876804,
          "__v": 0
        }
      }
	失败
	  {
        "status": 1,
        "msg": "此用户已存在"
      }

## 3. 更新用户
### 请求URL：
	http://localhost:5000/manage/user/update

### 请求方式：
	POST

### 参数类型

	|参数		|是否必选 |类型     |说明
	|_id         |Y       |string   |ID
    |username    |Y       |string   |用户名
    |password    |Y       |string   |密码
    |phone       |N       |string   |手机号
    |email       |N       |string   |邮箱
    |role_id     |N       |string   |角色ID

### 返回示例：
	成功:
	  {
        "status": 0,
        "user": {
          "_id": "5c3b382c82a14446f4ffb647",
          "username": "admin6",
          "password": "d7b79bb6d6f77e6cbb5df2d0d2478361",
          "phone": "13712341234",
          "email": "test@qq.com",
          "create_time": 1547384876804,
          "__v": 0
        }
      }
	失败
	  {
        "status": 1,
        "msg": "此用户已存在"
      }
    
## 4. 获取所有用户列表
## 5. 删除用户
## 6. 获取一级或某个二级分类列表
## 7. 添加分类
## 8. 更新品类名称
## 9. 根据分类ID获取分类
## 10. 获取商品分页列表
## 11. 根据ID/Name搜索产品分页列表
## 12. 添加商品
## 13. 更新商品
## 14. 对商品进行上架/下架处理
## 15. 上传图片
## 16. 删除图片
## 17. 添加角色
## 18. 获取角色列表
## 19. 更新角色(给角色设置权限)
## 20. 获取天气信息(jsonp)
