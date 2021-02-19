# luckysheet_django
luckysheet + django实现多人在线协同操作excel

QQ交流群: 697107880
```使用方法
使用起步：
1、安装python3.7
2、安装jdk，建议jdk8，因为我使用的就是该版本,因为当前py3的解压有bug (https://bugs.python.org/issue24301)
3、安装node.js
    安装
    npm install
    npm install gulp -g
    开发
    npm run dev
    打包
    npm run build
```
### 当前问题
1、新建一个sheet页的时候，如果别的客户端不点击这个新页面一下电话，那新建一方在新sheet页面的修改就不会被同步到其他客户端。因此别的客户端必须点击
一下新的sheet页，才能把新sheet页的修改同步过来。--2021/02/01

2、筛选功能，当前只能把添加筛选功能同步到其他客户端，无法把去除筛选功能同步到其他客户端。--2021/02/01

3、当前由于py3的gzip的bug冲突，所以暂时解压数据得使用java包了，[gzip的bug](https://bugs.python.org/issue24301) --2021/02/01

### 已解决问题
1、多人协同的时候，无法做到同步，卡在了返回值的这一步，返回格式未能对齐，单双引号导致的  --2021/02/01-问题已解决