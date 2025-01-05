## GIDSP 构建所需第三方jar包汇总
安装 maven 后，放入本地库文件夹
```
sudo apt install maven

cp -r * ~/.m2/repository/

```
### 手动安装方式
有些情况某些包可以需要安装多个版本
```
mvn install:install-file \
  -Dfile=rule-engine-jvm-3.2.2.jar \
  -DgroupId=org.fastable.gidsp.rules \
  -DartifactId=rule-engine-jvm \
  -Dversion=3.2.1 \
  -Dpackaging=jar
```
可以用高版本安装为低版本
```
mvn install:install-file \
  -Dfile=rule-engine-jvm-3.2.2.jar \
  -DgroupId=org.fastable.gidsp.rules \
  -DartifactId=rule-engine-jvm \
  -Dversion=3.1.0 \
  -Dpackaging=jar
```
