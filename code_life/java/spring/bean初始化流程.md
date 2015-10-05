# bean初始化流程

<!-- create time: 2015-05-10 22:10:52  -->

<!-- This file is created from $MARBOO_HOME/.media/starts/default.md
本文件由 $MARBOO_HOME/.media/starts/default.md 复制而来 -->


+ 执行构造方法

+ 执行set方法

+ 执行aware接口的方法

	(1) BeanNameAware接口的 setBeanName() 方法。
	
	(2) BeanClassLoaderAware 接口的 setBeanClassLoader() 方法。
	
	(3) BeanFactoryAware 接口的 setBeanFactory() 方法。
	
	(4) ResourceLoader接口的 set...() 方法。(ApplicationContext使用)
	
	(5) ApplicationEventPublisherAware 接口的 set...() 方法。(ApplicationContext使用)
	
	(6) MessageSourceAware 接口的 set...() 方法。(ApplicationContext使用)
	
	(5) ApplicationContextAware 接口的 set...() 方法。(ApplicationContext使用)
	
	(6) ServletContextAware 接口的 set...() 方法。(WebApplicationContext使用,仅对web有用)
	
+ 
	1)BeanPostProcessor的postProcessBeforeInitialization方法
	
	2)@PostConstruct

	3)InitializingBean的afterPropertiesSet方法
	
	4)init-method方法
	
	5)BeanPostProcessor的postProcessAfterInitialization方法
	
	
	
	
	
