# javaDiary
javaDiary


```java

// 代码自动生成器
public class KuangCode {
public static void main(String[] args) {
// 需要构建一个 代码自动生成器 对象
AutoGenerator mpg = new AutoGenerator();
// 配置策略
// 1、全局配置
GlobalConfig gc = new GlobalConfig();
String projectPath = System.getProperty("user.dir");
gc.setOutputDir(projectPath+"/src/main/java");
gc.setAuthor("狂神说");
gc.setOpen(false);
gc.setFileOverride(false); // 是否覆盖
gc.setServiceName("%sService"); // 去Service的I前缀
gc.setIdType(IdType.ID_WORKER);
gc.setDateType(DateType.ONLY_DATE);
gc.setSwagger2(true);
mpg.setGlobalConfig(gc);
//2、设置数据源
DataSourceConfig dsc = new DataSourceConfig();
dsc.setUrl("jdbc:mysql://localhost:3306/kuang_community?
useSSL=false&useUnicode=true&characterEncoding=utf-8&serverTimezone=GMT%2B8");
dsc.setDriverName("com.mysql.cj.jdbc.Driver");
dsc.setUsername("root");
dsc.setPassword("123456");
dsc.setDbType(DbType.MYSQL);
mpg.setDataSource(dsc);
//3、包的配置
PackageConfig pc = new PackageConfig();
pc.setModuleName("blog");
pc.setParent("com.kuang");
pc.setEntity("entity");
pc.setMapper("mapper");
pc.setService("service");
pc.setController("controller");
mpg.setPackageInfo(pc);
//4、策略配置
StrategyConfig strategy = new StrategyConfig();
strategy.setInclude("blog_tags","course","links","sys_settings","user_record","
user_say"); // 设置要映射的表名
strategy.setNaming(NamingStrategy.underline_to_camel);
strategy.setColumnNaming(NamingStrategy.underline_to_camel);
strategy.setEntityLombokModel(true); // 自动lombok；
strategy.setLogicDeleteFieldName("deleted");
// 自动填充配置
TableFill gmtCreate = new TableFill("gmt_create", FieldFill.INSERT);
TableFill gmtModified = new TableFill("gmt_modified",
FieldFill.INSERT_UPDATE);
ArrayList<TableFill> tableFills = new ArrayList<>();
tableFills.add(gmtCreate);
tableFills.add(gmtModified);
strategy.setTableFillList(tableFills);
// 乐观锁
strategy.setVersionFieldName("version");
strategy.setRestControllerStyle(true);
strategy.setControllerMappingHyphenStyle(true); //
localhost:8080/hello_id_2
mpg.setStrategy(strategy);
mpg.execute(); //执行
}
}

```
```javascript
6ZUMD7WWWU-eyJsaWNlbnNlSWQiOiI2WlVNRDdXV1dVIiwibGljZW5zZWVOYW1lIjoiSmV0cyBHcm91cCIsImFzc2lnbmVlTmFtZSI6IiIsImFzc2lnbmVlRW1haWwiOiIiLCJsaWNlbnNlUmVzdHJpY3Rpb24iOiIiLCJjaGVja0NvbmN1cnJlbnRVc2UiOmZhbHNlLCJwcm9kdWN0cyI6W3siY29kZSI6IklJIiwiZmFsbGJhY2tEYXRlIjoiMjAxOS0wOS0wMyIsInBhaWRVcFRvIjoiMjAyMC0wOS0wMiJ9LHsiY29kZSI6IkFDIiwiZmFsbGJhY2tEYXRlIjoiMjAxOS0wOS0wMyIsInBhaWRVcFRvIjoiMjAyMC0wOS0wMiJ9LHsiY29kZSI6IkRQTiIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDktMDMiLCJwYWlkVXBUbyI6IjIwMjAtMDktMDIifSx7ImNvZGUiOiJQUyIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDktMDMiLCJwYWlkVXBUbyI6IjIwMjAtMDktMDIifSx7ImNvZGUiOiJHTyIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDktMDMiLCJwYWlkVXBUbyI6IjIwMjAtMDktMDIifSx7ImNvZGUiOiJETSIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDktMDMiLCJwYWlkVXBUbyI6IjIwMjAtMDktMDIifSx7ImNvZGUiOiJDTCIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDktMDMiLCJwYWlkVXBUbyI6IjIwMjAtMDktMDIifSx7ImNvZGUiOiJSUzAiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA5LTAzIiwicGFpZFVwVG8iOiIyMDIwLTA5LTAyIn0seyJjb2RlIjoiUkMiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA5LTAzIiwicGFpZFVwVG8iOiIyMDIwLTA5LTAyIn0seyJjb2RlIjoiUkQiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA5LTAzIiwicGFpZFVwVG8iOiIyMDIwLTA5LTAyIn0seyJjb2RlIjoiUEMiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA5LTAzIiwicGFpZFVwVG8iOiIyMDIwLTA5LTAyIn0seyJjb2RlIjoiUk0iLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA5LTAzIiwicGFpZFVwVG8iOiIyMDIwLTA5LTAyIn0seyJjb2RlIjoiV1MiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA5LTAzIiwicGFpZFVwVG8iOiIyMDIwLTA5LTAyIn0seyJjb2RlIjoiREIiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA5LTAzIiwicGFpZFVwVG8iOiIyMDIwLTA5LTAyIn0seyJjb2RlIjoiREMiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA5LTAzIiwicGFpZFVwVG8iOiIyMDIwLTA5LTAyIn0seyJjb2RlIjoiUlNVIiwiZmFsbGJhY2tEYXRlIjoiMjAxOS0wOS0wMyIsInBhaWRVcFRvIjoiMjAyMC0wOS0wMiJ9XSwiaGFzaCI6IjE0Mjg5NzUwLzAiLCJncmFjZVBlcmlvZERheXMiOjcsImF1dG9Qcm9sb25nYXRlZCI6ZmFsc2UsImlzQXV0b1Byb2xvbmdhdGVkIjpmYWxzZX0=-Gd8RATyTEnHcAydKuC7N1ZdeLaMP9IR+nlPyVxvLsczAUTGKxcuAYbfz/uVtepg8ey4NfJlPNS+AGcGz8x7ImkX9jEV9KElMxPu3tKSdF/WKo6JCONX7UtudYa/9EQum3banxci/qH7jejSrFZSN+YjWQiYTR0Q8gq4/a2RyQTgseZfpImY/nXkOWLwWArr/p+4ddp/bWQN4nLTW+Z4ZaQeLE96Z9viCdn62EKOcR02Hfr9Oju9VYQh1L8pGrTqNey5nUSv/LQUbVwo5qoYbBRos8l6ewkFNGsuC3vtOgGWSgkgChbDjWhW4Nkm4vDM2NFAphMsS1dgyPw3eJ3C+6A==-MIIElTCCAn2gAwIBAgIBCTANBgkqhkiG9w0BAQsFADAYMRYwFAYDVQQDDA1KZXRQcm9maWxlIENBMB4XDTE4MTEwMTEyMjk0NloXDTIwMTEwMjEyMjk0NlowaDELMAkGA1UEBhMCQ1oxDjAMBgNVBAgMBU51c2xlMQ8wDQYDVQQHDAZQcmFndWUxGTAXBgNVBAoMEEpldEJyYWlucyBzLnIuby4xHTAbBgNVBAMMFHByb2QzeS1mcm9tLTIwMTgxMTAxMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxcQkq+zdxlR2mmRYBPzGbUNdMN6OaXiXzxIWtMEkrJMO/5oUfQJbLLuMSMK0QHFmaI37WShyxZcfRCidwXjot4zmNBKnlyHodDij/78TmVqFl8nOeD5+07B8VEaIu7c3E1N+e1doC6wht4I4+IEmtsPAdoaj5WCQVQbrI8KeT8M9VcBIWX7fD0fhexfg3ZRt0xqwMcXGNp3DdJHiO0rCdU+Itv7EmtnSVq9jBG1usMSFvMowR25mju2JcPFp1+I4ZI+FqgR8gyG8oiNDyNEoAbsR3lOpI7grUYSvkB/xVy/VoklPCK2h0f0GJxFjnye8NT1PAywoyl7RmiAVRE/EKwIDAQABo4GZMIGWMAkGA1UdEwQCMAAwHQYDVR0OBBYEFGEpG9oZGcfLMGNBkY7SgHiMGgTcMEgGA1UdIwRBMD+AFKOetkhnQhI2Qb1t4Lm0oFKLl/GzoRykGjAYMRYwFAYDVQQDDA1KZXRQcm9maWxlIENBggkA0myxg7KDeeEwEwYDVR0lBAwwCgYIKwYBBQUHAwEwCwYDVR0PBAQDAgWgMA0GCSqGSIb3DQEBCwUAA4ICAQAF8uc+YJOHHwOFcPzmbjcxNDuGoOUIP+2h1R75Lecswb7ru2LWWSUMtXVKQzChLNPn/72W0k+oI056tgiwuG7M49LXp4zQVlQnFmWU1wwGvVhq5R63Rpjx1zjGUhcXgayu7+9zMUW596Lbomsg8qVve6euqsrFicYkIIuUu4zYPndJwfe0YkS5nY72SHnNdbPhEnN8wcB2Kz+OIG0lih3yz5EqFhld03bGp222ZQCIghCTVL6QBNadGsiN/lWLl4JdR3lJkZzlpFdiHijoVRdWeSWqM4y0t23c92HXKrgppoSV18XMxrWVdoSM3nuMHwxGhFyde05OdDtLpCv+jlWf5REAHHA201pAU6bJSZINyHDUTB+Beo28rRXSwSh3OUIvYwKNVeoBY+KwOJ7WnuTCUq1meE6GkKc4D/cXmgpOyW/1SmBz3XjVIi/zprZ0zf3qH5mkphtg6ksjKgKjmx1cXfZAAX6wcDBNaCL+Ortep1Dh8xDUbqbBVNBL4jbiL3i3xsfNiyJgaZ5sX7i8tmStEpLbPwvHcByuf59qJhV/bZOl8KqJBETCDJcY6O2aqhTUy+9x93ThKs1GKrRPePrWPluud7ttlgtRveit/pcBrnQcXOl1rHq7ByB8CFAxNotRUYL9IF5n3wJOgkPojMy6jetQA5Ogc8Sm7RG6vg1yow==
```
