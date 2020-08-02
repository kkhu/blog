# Kotlin 

在kotlin中，程序都会包含一个main()函数，作为程序的入口。
        
        fun main(args: Array<String>) {  
            // TODO  
        }
## 语法  
### 注释
##### 单行
// 加法
fun add() {
} 
##### 多行
/* */
##### 文档注释
/**  */

## 数据类型  
### 变量
#### 变量的申明
var 变量名：数据类型  
val 变量名：数据类型

var 申明可变变量    
val 申明不可变变量

var age: Int = 28;
val gender: short = 1;

### 基本数据类型
Byte, Short, Int, Long, Float, Double  

| 类型名 | 描述 | 占用空间 | 
| ----- | ----| ------- |
| Byte | 字节 | 8位（1个字节） |
| Char  | 字符型 | 16位（2个字节）|
| Short  | 短整型 | 16位（2个字节）|
| Int | 整型 | 32位（4个字节） |
| Long | 长整型 | 32位（4个字节） |
| Float | 浮点型 | 64位（8个字节） |
| Double | 双精度浮点型 | 64位（8个字节） |
| Boolean | 布尔类型 ||

注：  
Char用于存储一个单字符，与Java不同的是Char不能直接赋值为数字。  

数组创建  
方式一：  
var nums: IntArray = intArrayOf(1, 2, 3);  
var boos: BooleanArray = booleanArrayOf(true, false, false);  
var chars: CharArray = charArrayOf('a', 'b', 'c');  

方式二：
var nums: Array<Int> = arrayOf(1, 2, 3);  
var boos: Array<Boolean> = arrayOf(true, false, false);  
var chars: Array<Char> = arrayOf('a', 'b', 'c');  

注：  
在kotlin中不能使用stringArrayOf方法创建数组，因为String不属于基本数据类型。需要使用Array<String>  

字符串数组  
var str: Array<String> = arrayof(“hello", "world");  

## 操作符  
### 运算符 
##### 算术运算符  
| 运算符 | 运算 | 范例 | 结果 | 
| ----- | ----| ------- | --- |
| + | 加 | 2 + 2 |  |
| - | 减 | 2 - 2 |  |
| * | 乘 | 2 * 2 |  |
| / | 除 | 2 / 2 |  |
| % | 取余 | 2 % 2 |  |
| .. | 范围 | a=1; b = a..2; |  |
| ++ | 自增 | a=1; a++; |  |
| -- | 自减 | a=1; a--; |  |

##### 赋值运算符  
| 运算符 | 运算 | 范例 | 结果 | 
| ----- | ----| ------- | --- |
| = | 赋值 | a=6; b=5; | a=6; b=5; |
| += | 加等于 | a=6; b=5; a+=b; | a=11; b=5; |
| -= | 减等于 | a=6; b=5; a-=b; | a=1; b=5; |
| *= | 乘等于 | a=6; b=5; a*=b; | a=30; b=5; |
| /= | 除等于 | a=6; b=5; a/=b; | a=1; b=5; |
| %= | 模等于 | a=6; b=5; a%=b; | a=1; b=5; |

##### 比较运算符
| 运算符 | 运算 | 范例 | 结果 | 
| ----- | ----| ------- | --- |
| == | 等于 | a=6; b=5; a==b; | false |
| != | 不等于 | a=6; b=5; a!=b;| true |
| < | 小于 | a=6; b=5; a<b; | false |
| > | 大于 | a=6; b=5; a>b; | true |
| <= | 小于等于 | a=6; b=6; a<=b; | true |
| >= | 大于等于 | a=6; b=5; a>=b; | true |

##### 逻辑运算符
| 运算符 | 运算 | 范例 | 结果 | 
| ----- | ----| ------- | --- |
| && | 与 |  |
| &vert; &vert;  | 或 |  |
| ! | 非 |  |

## 语句  
#### 选择结构语句
    if (expression) {
        // TODO  
    }
    
    if (expression) {
        // TODO  
    } else {
        // TODO  
    }
    
    if (expression) {
        // TODO  
    } else if (expression) {
        // TODO  
    } else {
        // TODO  
    }

三元运算符  
判断条件 ? 表达式1 ： 表达式2;  

when条件语句  
    when (expression) {  
        1 -> print("1")  
        12 -> print("2")  
    }  

#### 循环语句  
##### while 循环语句  
    while (expression) {
        // TODO  
    }

##### do...while 循环语句  
    do {
        // TODO  
    } while (expression)
    
##### for 循环语句  
    for (循环对象 in 循环条件) {
        // TODO  
    }

##### forEach 循环语句  
arr.forEach() {
    // TODO  
}

#### 类型转换 
##### 强制类型转换  
通过as操作符进行强制类型转换  
例：
var a = "1";
var b: String = a as String;

安全调用符： ?.  
Elvis操作符： ?:  
    如果当前变量为空可指定默认值  
非空断言： !!.  
    非空断言(!!.)会将任何变量转换为非空类型的变量，若该变量为空则抛出异常  



## 函数  
函数又称方法，是具有特定功能的一段独立程序。  
函数都有：函数关键字 函数名 函数参数 函数返回值  

#### 函数语法
    
    fun add(a: Int, b:Int): Int {
        return a + b;
    }

##### 表达式函数  
如果函数体中只有一行代码，则可以把包裹函数体的花括号{}替换成“=”，把函数体放在“=”的后面，这样的函数称为单表达式函数。

fun add(a: Int, b:Int): Int = a + b;

## 面向对象  
面向对象(Object Oriented) 是一种符合人类思维习惯的编程思想。  

面向对象特性：封装、继承和多态  

封装  
将对象的属性和行为封装起来，不需要让外界知道具体的实现细节。 

继承  
继承主要描述类与类之间的关系，通过继承可以在无须重新编写原有类的情况下，对原有类的功能进行扩展。  

多态  
多态是指在程序中允许出现重名现象，它指在一个类定义的属性和方法被其继承后，它们可以具有不同的数据类型或表现出不同的行为。 

### 类和对象  
#### 类的定义  
类是对象的抽象，它用于描述一组对象的共同特征和行为。  

    class Person {
        // 成员属性 
        private var name = "";
        private var age = 0;
        private fun sayHello() {
            println("My name is ${name}")
        }
    }

对象的创建  
kotlin中创建类的对象不需要new  
    var p = Person();

#### 构造函数  
Kotlin中的构造函数分为两种，主构造函数和次构造函数； 构造函数使用contructor关键字进行修饰，一个类可以有一个主构造函数和多个次构造
函数。  
如果主构造函数没有任何注解或可见修饰符（如public）,constructor关键字可省略。  

定义  
class 类名  constructor([形参1， 形参2]) {}   

次构造函数，同样使用constructor关键字定义，只不过次构造函数位于类体中。次构造函数必须调用主构造函数或其它次构造函数，其调用方式为
“次构造函数：this(参数列表)”

#### 类的继承  
Kotlin中所有的类都默认使用final关键字修饰，不能被继承，因此,当继承某个类时，需要在这个类的前面加上open关键字。如果不open关键字编译不通过。
在Kotlin中一个类只能继承一个父类。    

    open class Message {
        fun addMsg(msg: String) {
            println("Message add msg=${msg}");
        }
    }
    class TextMessage: Message() {
        fun addTextMsg(msg: String) {
            println("TextMessage add msg=${msg}");
            super.addMsg(msg);
        }
    }
    
#### 方法的重写  
方法的重写使用override关键字标识；在父类中需要被重写的属性和方法前必须使用open关键字来修饰。  

#### super关键字  
在Kotlin中使用super关键字访问父类的成员。  
super.成员变量  
super.成员方法  

注：  
Kotlin中所有类都继承Any类，它是所有类的父类，如果一个类在声明时没有指定父类，则默认父类为Any类。 
在程序运行时，Any类会自动映射为Java中的java.lang.Object类。    

### 抽象类和接口  
#### 抽象类  
使用abstract关键字修饰类和方法  

#### 接口  
使用interface关键字来定义接口, 接口可以继承接口。    
    
    interface Message {
        fun addMsg(msg: String);
    }

通过冒号 (:) 实现接口，一个类可以实现多个接口  

#### 嵌套类  
在没有任何修饰的情况下，定义在一个类内部的类默认称为嵌套类。  
嵌套类无法访问外部类的成员。  

#### 内部类  
对一个嵌套类添加inner修饰符表示为一个内部类。  
内部类可以访问外部类的成员。  

#### 枚举类  
使用enum修饰的类  

#### 密封类  
使用sealed关键字修饰  
密封类用于表示受限制的类层次结构，当一个值只能在一个集合中取值，而不能取其它值时，此时可以使用密封类。
在某种意义上，密封类是枚举类的扩展，即枚举类型的值的集合。  

#### 数据类  
使用data关键字修饰  

### 异常
#### 异常处理  

    try {
        // 代码块
    } catch (e: SomeException) {
    } finally {
    }

### 集合  
#### List  
List 是有序可重复的集合  

#### Set 
Set 是无序元素不可重复的集合

List 和 Set都继承自Collection接口  

### 输出语句
方法  
        println()


### Kotlin与Java的区别
#### 相同点  
1.Kotlin是严格区分大小写的
2.都是面向对象的语言有类，抽象类，继承，接口，对象，等概念
#### 不同点  
1.在kotlin里Char只能存储字符，而在Java里可以存储数字。  
2.创建类的对象，在kotlin里不需要使用new关键字，在Java或其它语言里需要使用new 关键字。  
