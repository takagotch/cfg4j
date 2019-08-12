### cfg4j
---
https://github.com/cfg4j/cfg4j

```java
public class Cfg4jPoweredApplication {
  public interface SampleConfig {
    Integer birthYear();
    List<String> friends();
    URL homepage();
    Map<String, Charater> grades();
  }
  
  public static void main(String... args) {
    ConfigurationSource source = new GitConfigurationSourceBuilder()
      .withRepositoryURI("https://github.com/cfg4j/cfg4j-git-sample-config.git")
      .build();
      
    ConfigurationProvider provider = new ConfigurationProviderBuilder()
      .withConfigurationSource(source)
      .build();
      
    SampleConfig config = configurationProvider.bind("reksio", SampleConfig.class);
    
    System.out.println(config.homepage());
  }
}
```

```
```

```
```
