22-05-18  SUNNY  
### encapsulation 封装  
把抽象出的数据（属性）和对数据的操作（方法）封装在一起。  
数据保存在内部，程序的其他部分必须通过被授权的操作（方法），  
才能对数据进行操作。保护了数据的安全性。  
       
  #### 封装的好处  
  隐藏实现细节  
  可以对数据进行验证，保证安全合理  
    
  #### 封装实现的步骤      
1. 把属性私有化
1. 提供公共的set方法，对属性进行判断及赋值  
1. 提供公共的get方法，用于获取属性的值    

可以用快捷键快速generate（生成） getter 和 setter  
// setter 示例  
```

public void setName(String name) {
     if (name.length() >= 2) {  //判断输入的信息是否正确
         this.name = name;      //正确则赋值
     } else {                   //错误则提示并赋默认值
         System.out.println("Error. Name length should > 2  . Default name = Joe");
         this.name = "Joe";
     }
 }
```  

// getter示例  
~~~

public String getName() {
     return name;
 }
~~~  

// 还可以在getter中加入校验信息，没有权限则不显示  
```
public double getBalance(String passcode) {
    //if passcode is correct ,show balace
    if (passcode.equals(this.passcode)) {
        return balance;
    } else {
        System.out.println("Wrong password. balance can't be seen.");
        return 0;
    }
}
```  
//  如果想快捷show info 可以不用自己定义show info 方法  
//  可以快捷键generate 一个toString方法，已有模板  

```
public String toString() {
    return "Account{" +
            "name='" + name + '\'' +
            ", passcode='" + passcode + '\'' +
            ", balance=" + balance +
            '}';
}
```  

//输出结果如下：  
```
Account{name='Joe', passcode='234567', balance=230.4}
```


 
