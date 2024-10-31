## Note
This project is the java implementation of tls-sig-api-v2. Previous asymmetric keys cannot use APIs of this version. To enable them to use APIs of this version,[see here](https://github.com/tencentcloud/tls-sig-api-java).
## Integration
### maven
``` xml
<dependencies>
    <dependency>
        <groupId>com.github.tencentcloud</groupId>
        <artifactId>tls-sig-api-v2</artifactId>
        <version>2.0</version>
    </dependency>
</dependencies>
```

### gradle
```
dependencies {
    compile 'com.github.tencentcloud:tls-sig-api-v2:2.0'
}
```

### source code
``` shell
./gradlew -b user_build.gradle build
```
The generated jar can be found under `build/libs`. You can download it by yourself by relying on org.json.
## use
``` java
import com.tencentcloud.TLSSigAPIv2;

TLSSigAPIv2 api = new TLSSigAPIv2(1400000000, "5bd2850fff3ecb11d7c805251c51ee463a25727bddc2385f3fa8bfee1bb93b5e");
System.out.print(api.genUserSig("xiaojun", 180*86400));
```
