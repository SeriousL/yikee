

## 使用angularjs

1. 项目部署环境搭建 视图 js libs分别放置 方便日后维护
2. 创建单页面应用 使用锚点 + 路由
3. 使用路由 需要配置路由  配置好模板视图的链接和对应视图对应的控制器
4. run运行模块($rootscope服务)   创建全局方法 toggle函数 控制页面的滑动 因为此函数 在页面中被多次调用 在全局$rootscope上创建 app中都可以访问到
5. 添加左侧列表中的菜单项的滑动动画  这个动画需要操作dom元素 在toggle函数中 定义 
6. 如果在 在run中toggle外定义 此时获取不到dom元素 因为配置和运行是在angular解析指令之前,此时还没有dd这些元素
7. 创建控制器模块  并加入到index页面 并在Yike这个模块中引入这个依赖
8. 控制器模块中创建导航菜单控制器  生成每个dd
9. 创建 today older 等控制器
10. 处理细节 loading图片  创建自定义指令 在$http回调函数中控制
11. 处理顶部标题 在每个单独的控制器中创建全局的变量title 每个控制器对应自己的名字
12. 处理左侧菜单选中问题  每个dd再选中是才有样式 也就是变色   使用ng-class  定义全局变量每个控制器有个单独的key  在遍历dd时 给每个dd都加上一个$index索引, 判断索引是不是和对应控制器中的索引相同.