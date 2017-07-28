
Spring与SpringMVC整合要注意的是，Spring容器与SpringMVC容器是两个容器，存在父子关系，SpringMVC容器在Spring容器里面，SpringMVC容器可以访问Spring容器里面的bean，反之则不行，所以最好将Spring的配置文件和SpringMVC的配置文件分开。另外根据官方推荐，SpringMVC与Spring整合时，SpringMVC容器中放Controller层的bean，Spring容器中则放除了Controller之外的bean。官方推荐配置如下
> SpringMVC配置文件

        <!-- 启动自动扫描，use-default-filters默认为true，当此属性为true时，include-filer会失效，他不仅会扫描include-filter包含的内容，还会去扫面其他内容，所以要关闭默认属性-->
        <context:component-scan base-package="com.pgb" use-default-filters="false">
            <!-- 制定扫包规则 ,只扫描使用@Controller注解的JAVA类 -->
            <context:include-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
        </context:component-scan>

> Spring配置文件

        <context:component-scan base-package="com.pgb">
		    <context:exclude-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
	    </context:component-scan>
