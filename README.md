# 创建步骤
1. 创建github仓库
2. 拉取创建的仓库到本地
3. composer init #初始化当前目录配置，填写包括报名、作者、版本等。
4. composer dump-autoload 自动加载文件
5. 推送到github仓库中

# 使用
```php
#修改composer.json文件
   "require": {

        "pack/hyx": "dev-main"
    },
    "repositories": {
        "0": {
            "type": "git",
            "url": "https://github.com/DMC-HYX/my-composer-pack.git"
        }
    }
# 最后composer update

# 使用方法
路径：routes/web.php
//=======调用自定义composer组件
Route::any('myself',function(){
    $obj=new \Pack\Hyx\Service();
    dd($obj->hello());
});
```
