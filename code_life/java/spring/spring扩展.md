# spring扩展

<!-- create time: 2015-05-07 23:22:06  -->

<!-- This file is created from $MARBOO_HOME/.media/starts/default.md
本文件由 $MARBOO_HOME/.media/starts/default.md 复制而来 -->

**有哪些地方可以， how do**
****


+ #####BeanFactoryPostProcessor 类实例化前的处理，比如替换原来类 

+ #####BeanPostProcessor 类实例化后的处理，比如自定义类注解来实现属性的处理

+ #####在方法上自定义注解可以用aop去拦截

+ #####FactoryBean 

	demo如下

	```xml
	<bean id="myBean" class="MyFactoryBean"/>
	```
	```java
	 MyFactoryBean implements FactoryBean<User> {
	    public Userget Object() throws Exception {
	        return new User();
	    }
	}
	```
	id为myBean的类实际上User类，而不是MyFactoryBean。
	比如dubbo中
	
	```xml
	<dubbo:reference id=“xxxService1” interface=“com.xxx.XxxService1” />
	<dubbo:reference id=“xxxService2” interface=“com.xxx.XxxService2” />
	```
	实际上xxxService1 xxxService2 都会初始化一个FactoryBean，FactoryBean根据不同的interface参数返回不同的代理对象。
	这样可以依靠spring的注解注入。

+ #####InitializingBean and DisposableBean
 
+ #####ApplicationContextAware

+ #####init-method and destroy-method

+ #####自定义标签  
	1)定义xsd<br/>
	2)定义NamespaceHandlerSupport和BeanDefinitionParser。自定义的NamespaceHandlerSupport中调用自定义的BeanDefinitionParser<br/>
	3)spring.handlers关联命名空间和NamespaceHandlerSupport。spring.shcemas关联命名空间和xsd文件位置  spring会去加载spring.*.jar/META-INF下的这两个配置文件
	
	
<br/><br/>
	
####注意事项
	需要注意spring对扩展点的执行顺序,下面是几个易混淆的点的执行顺序。
	1)BeanPostProcessor的postProcessBeforeInitialization方法
	2)InitializingBean的afterPropertiesSet方法
	3)init-method方法
	4)BeanPostProcessor的postProcessAfterInitialization方法
	
	
	
	
	



