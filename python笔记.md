# 单下划线、双下划线的意义与作用
单下划线开头

    属性或方法名以单下划线开头它表示该方法或者属性是该类型的私有方法或属性。但其实在Python中不存在真正意义上的私有方法或者属性，前面加单下划线_只是表示你不应该去访问这个方法或者属性，因为它不是API的一部分。

双下划线开头

    表示私有。为了避免子类覆盖父类的方法。
    
开头结尾双下划线

    开头结尾都加双下划线的方法表示这是Python自己调用的，你不要调用。
    
    
# 实例方法、类方法、静态方法的区别与作用
实例方法

    定义：第一个参数必须是实例对象，该参数名一般约定为“self”，通过它来传递实例的属性和方法（也可以传类的属性和方法）；

    调用：只能由实例对象调用。

类方法

    定义：使用装饰器@classmethod。第一个参数必须是当前类对象，该参数名一般约定为“cls”，通过它来传递类的属性和方法（不能传实例的属性和方法）；将类本身作为对象进行操作的方法。

    调用：实例对象和类对象都可以调用。

静态方法

    定义：使用装饰器@staticmethod。参数随意，没有“self”和“cls”参数，但是方法体中不能使用类或实例的任何属性和方法；静态方法是类中的函数，不需要实例。静态方法主要是用来存放逻辑性的代码，逻辑上属于类，但是和类本身没有关系，也就是说在静态方法中，不会涉及到类中的属性和方法的操作。可以理解为，静态方法是个独立的、单纯的函数，它仅仅托管于某个类的名称空间中，便于使用和维护。

    调用：实例对象和类对象都可以调用。
# Python 字符串前面加u,r,b的含义
字符串前加u

    后面字符串以 Unicode 格式 进行编码，一般用在中文字符串前面，防止因为源码储存格式问题，导致再次使用时出现乱码。
    
字符串前加r

    禁止字符转义，常用于正则表达式，对应着re模块。
    
字符串前加b

    b''前缀表示：后面字符串是bytes 类型。网络编程中，服务器和浏览器只认bytes 类型数据。
    在 Python3 中，bytes 和 str 的互相转换方式是
    str.encode('utf-8')
    bytes.decode('utf-8')
