# java内部类

>
>
>见《疯狂java讲义》P205

分类：

1. 成员内部类
   * 静态内部类
   * 非静态内部类
2. 局部内部类（包含匿名内部类）



* 内用外，随意访问（包括private修饰的）；外用内，必须用对象的形式
* 不允许同一个包中的其他类访问内部类
* 非静态内部类不能拥有静态成员

### 概念说明：

**成员内部类**：

定义在外部类中的类叫成员内部类

**局部内部类**

定义在方法中的内部类

### 成员内部类

**成员内部类的定义**

~~~java
public class OuterClass{
    //此处定义内部类，格式与外部类相同
}
~~~



**在其他类中使用内部类的方法**

1. 间接方式：在外部类方法中，使用内部类，然后在其他类中调用外部类的方法

2. 直接方式：公式法实例化  `外部类名称.内部类名称  对象名 = new 外部类名称().new 内部类名称();`

   前提是内部类是  `public`  修饰的

**变量名重名的处理：**

>
>
>num就是最近的变量（下面的例子是局部变量）
>
>this.num是内部的成员变量
>
>Outer.this.num是外部的成员变量

![](https://geda-1302176138.cos.ap-nanjing.myqcloud.com/img/overname.png)

**静态内部类和非静态与他们的内部类关系**

| 类           | 与外部类的关系                                               |
| ------------ | ------------------------------------------------------------ |
| 非静态内部类 | 依附于外部类对象存在，即当非静态内部类对象存在时，必定存在外部类的对象 |
| 静态内部类   | 依附于外部类，它不是寄生在外部类的实例对象中的，当静态内部类对象存在时，并不需要外部类对象 |

因此，只要是静态内部类，它只能使用外部类的静态成员



### 局部内部类

==“局部”:只有当前所属的方法才能使用它，出了这个方法外面就不能用了。==

==它没有权限修饰符也不能被static修饰==

**局部内部类的定义**

~~~java
public class outerClass
{
    //外部类的方法
    public void Outermethod()
    {
        //此处定义内部类
        //但是该类没有修饰符
    }
        
}
~~~

==注意：==

局部内部类，如果希望访问所在方法的局部变量，那么这个局部变量必须是[有效final的]。

~~~java
public class outerClass{
    int num=10;
    public class inner{
        System.out.println(num);
        //因为num只赋值了一次，这里num并未改变，所以不会报错
        //为了保险，需要将外部类的num设置为final的常量
    }
}
~~~

分析:

为了防止成员变量先消亡的情况

![](https://raw.githubusercontent.com/Ge-daye/imges/master/images/final.png)

![](https://geda-1302176138.cos.ap-nanjing.myqcloud.com/img/final2.png)





### 匿名内部类

语法

~~~java
new 实现接口（）
{
 //匿名内部类类体，包含接口的所有抽象方法   
}

或者
new 父类的构造器（参数列表）
{
    //匿名内部类的类体，要包含父类中的所有抽象abstract方法
}
~~~

匿名内部类必须继承一个父类或者实现一个接口，但是最多只能继承一个父类或一个接口

**注意事项**

1. 匿名内部类不能是抽象类
2. 因为没有类名，匿名内部类不能定义构造器
3. 创建匿名内部类时，必须实现接口或抽象父类里的所有抽象方法，如果有需要，也可以重写父类中的普通方法

![](https://raw.githubusercontent.com/Ge-daye/imges/master/images/aa11.png)