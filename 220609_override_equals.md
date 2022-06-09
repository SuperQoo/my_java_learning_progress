```
//新建一些人物，给属性赋值
Person jack = new Person("alex", 25, 'm');
Person p1 = new Person("alex", 25, 'm');
Person p2 = new Person("alex", 25, 'f'); 
Person rose = new Person("rose", 24, 'f');
Person p3 = rose;
```

```
//未重写equals方法前
alex.equals(p1); //false，因为两者地址不同
alex.equals(p2); //false，地址不同、属性也不同
rose.equals(p3); // true，指向同一地址（对象）
```

```
// 我重写的equals方法,很累赘,后面有优化版
public boolean equals(Object obj) {
    if (this == obj) {
        return true;    //同个对象直接返回true
    }
    if (obj instanceof Person) { //判定是否为Person类
        if (name.equals(((Person) obj).getName())
            && age == ((Person) obj).getAge()
            && gender == ((Person) obj).getGender()) {
            return true; //各项属性皆相同，返回true
        }
    }
    return false;   //不满足上述条件即返回false
}
```

```
// 重写equals方法后
alex.equals(p1); // true，因为重写后的equals判断属性相同即可返回true
alex.equals(p2); //false，两者gender属性不同
rose.equals(p3); // true，两者指向同一对象，认为相同
```

其实重写的equals方法可以优化成下面的样子  
对传入对象的属性不需要用 `getter`  
因为这个`equals()`方法也在`Person`类里  
类内可以直接访问被 `private` 修饰的属性  
```
public boolean equals(Object obj) {
    if (this == obj) {
        return true;    //同个对象直接返回true
    }
    if (obj instanceof Person) { //判定是否为Person类
        Person p = (Person)obj; //改个名字下面比较方便写
        return name.equals(p.name) && age == p.age() && gender == p.gender()) 
    }
    return false;   //不满足上述条件即返回false
}
```