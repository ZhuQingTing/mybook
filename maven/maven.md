# maven 

## 依赖范围scope

* Compile 

  默认配置。编译/测试/运行阶段均生效。

* Test

  仅测试生效

* Provided

  编译/测试生效，运行时无效。如servlet-api，运行时容器已提供。

* Runtime

  测试/运行时生效。如jdbc驱动。

* System

  编译/测试生效，需要通过systemPath元素指定依赖本地文件。

  ```xml
  <dependency>
      <groupId>javax.sql</groupId>
      <artifactId>jdbc-stdext</artifactId>
      <version>2.0</version>
      <scope>system</scope>
      <systemPath>${java.home}/lib/rt.jar</systemPath>
  </dependency>
  ```

* Import

  不会对编译/测试/运行产生实际影响。

## 依赖传递

|          | compile  | test | provided | runtime  |
| -------- | -------- | ---- | -------- | -------- |
| compile  | compile  | -    | -        | runtime  |
| test     | test     | -    | -        | test     |
| provided | provided | -    | provided | provided |
| runtime  | runtime  | -    | -        | runtime  |

注：列为第一直接依赖，行为第二直接依赖。



## 可选依赖 optional

optional=true时，依赖不会传递。

