@Component 已经可以支持声明一个 bean 了，为何还要再弄个 @Bean 出来？
解答：用@Configuration加上@Bean可以在一个类里注入多个bean，
而@Coponent只能一个类注入一个，不方便。
使用场景比如Redis的布隆过滤器，如果用XML需要繁琐的配置，且有很多路径字段，
可读性很差，用@Configuration加@Bean之后可以在类里清晰明白地看到是如何配置的。
而此时如果用@Component，需要创建大量的类。