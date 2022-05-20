2022-05-20 SUNNY  
#### extends 继承

  
  
  
    
在父类中定义共有属性以及共有方法，子类可以继承使用  
假设父类是学生类，学生的名字、年龄、分数是共有属性  
而学生不同科目的考试是特有方法（特有方法写在子类中）
```
public class Student {  //父类
    //    共有属性
    String name;
    private int age;
    private double score;

    //  共有方法
    public void setScore(double score) {
        this.score = score;
    }
    // doTest 考试方法不是公有方法，pupil和gradute有各自特有方法
    // 所以此处不写doTest方法

    @Override
    public String toString() {
        return "Student{" +
                "name='" + name + '\'' +
                ", age=" + age +
                ", score=" + score +
                '}';
    }
}
```  
Pupil类代表小学生，小学数学考试是小学生类的特有方法。
```
public class **Pupil extends Student** {
//    写它特有的属性及方法
    public void doTest(){
        System.out.println("小学生 "+ name +" 正在考**小学数学**");
    }
}
```
Graduate类代表大学生，大学数学考试是大学生类的特有方法。
```
public class Graduate extends Student {
//  写其特有属性 特有方法
    public void doTest(){
        System.out.println("研究生 "+ name +" 正在考**大学数学**");
    }
}
```
