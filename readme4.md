# 最基础的spring mvc配置

## 1.web.xml配置

spring-mvc配置文件以及spring url拦截。
http://chuantu.biz/t6/86/1507531674x2061759526.png

配置字符编码过滤器
http://chuantu.biz/t6/86/1507532133x2061759526.png

## 2.spring-mvc.xml配置

http://chuantu.biz/t6/86/1507532443x2061759526.png

这些就是spring mvc最基础的配置，下面是一个控制类的实例：

@Controller  
@RequestMapping("/start")     
public class StartController {  
  
    private static String START="module/jsp/start";  
       
    @RequestMapping("/index")     
    public String start(HttpServletRequest request){  
        return START;  
    }  
}

这样在浏览器中输入：http://localhost:8080/start/index即可访问到start.jsp页面
