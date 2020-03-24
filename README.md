# JavaEE_2020
<!-- JavaEE课程 -->


### Tomcat始终连接不上
**解决方法：**
最后搜寻整个磁盘后发现了两个不同版本的Tomcat，IDEA调用的版本不是系统配置的那个，修改后，依旧失败。最终删除另一个Tomcat后成功。

<br/>


### 运行出现异常，发现是未导入maven包

pom.xml文件中的配置未生效，发现是远端导入Jackson包失败。

**解决方法：**
网上下载依赖包，加入到lib文件夹下，修改pom.xml文件，添加如下语句,使其从本地读取依赖
```
    <scope>system</scope>
    <systemPath>${project.basedir}/lib/</systemPath>
```
<br/>

### 运行发现异常提示为Java xx版本不支持xxx
发现是IDEA设置Java版本过低，需要手动设置