22-05-14  CLOUDY  
### MODIFIER 访问修饰符  
用于控制方法和属性的访问权限

 | 访问修饰符| 访问级别 |  |
 | :---: | :---: | :--- |  
 | `public` | 公开级别 | 对外公开 |   
 | `protected` |受保护级别 | 对子类和同包类公开 |    
 | `不写` |默认级别 | 对同一个包的类公开 |   
 | `private` |私有级别 | 不对外公开，只有本类可以访问 |  
 
 | |同类 | 同包 | 子类 | 不同包 |  
 |:---: | :---: | :---: | :---: | :---: | 
 |`public`  | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |    
 |`protected` | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :x: |    
 |`不写` | :heavy_check_mark: | :heavy_check_mark: | :x: | :x: |    
 |`private` | :heavy_check_mark: | :x: | :x: | :x: |  
   
     
  







[语法](https://markdown.com.cn/basic-syntax/"Markdown语法")  

[*Markdown grammar*] [1]  
  
    
[1]: <https://markdown.com.cn/basic-syntax/> "Markdown grammar" 