# Flaskr实现笔记

1. 该系统用到了SQLAlchemy，用于访问数据库，使用`pip install SQLAlchemy`安装，没有依赖项
2. 创建目录结构：`mkdir flaskr  flaskr/static flaskr/templates`
3. 目前只有一张entries表，有三个字段：id（主键、AI）、title、text，详见`schema.sql`
4. 源码中设置了一些常量，包括了数据库路径等，可以用app.config.from_object获取
5. 使用`app.config.from_envvar`可以从环境变量加载配置项
6. 用`@app.before_request`标记请求前调用的函数，用`@app.teardown_request`结束后调用的函数
