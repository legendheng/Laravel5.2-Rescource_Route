# Laravel5.2-Rescource_Route
Laravel5.2使用资源路由resource 快速方便地新建控制器方法
### 第一步、在route.php里面建下面的资源路由
```php
Route::resource('test','TestController');
```
### 第二步、使用artisan命令新建TestController控制器，如下：
```php
php artisan make:controller TestController
```
### 第三步、使用artisan命令查看所有路由，如下：、
```php
php artisan route:list
```
### 按照上面的步骤可以得到如下的路由：
* public function index() //方法get的形式 路由为admin/category                        用于显示主页
* public function store() //方法post的形式 路由为admin/category                       用于处理添加提交
* public function create() //方法get的形式 路由为admin/category/create                用于显示添加
* public function show() //方法get的形式 路由为admin/category/{category}              用于显示单个内容
* public function destroy() //方法delete的形式 路由为admin/category/{category}        用于删除
* public function update($cate_id) //方法put的形式 路由为admin/category/{category}    用于处理更新
<br>这里视图页面需要加上
```html
<input type="hidden" name="_method" value="put">
```
* public function edit($cate_id) //方法get的形式路由为admin/category/{category}/edit  用于显示更新
