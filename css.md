## css基本
1. 用法  
``` css
<style>
    p{
        color:red;
        属性名:属性值;
    }
</style>
```
2. 三种引用方式  
    1. 行内引用
    ```css
    <p style="color:red;">
    ```
    2. 内部样式  
    ```css
    <style>
    p{
        color:red;
        属性名:属性值;
    }
    </style>
    ```
    3. 外部样式  
    ```html
    <link rel='stylesheet' type='text/css' href='static/index.css'>
    ```
## 选择器
### 基本选择器
1. 标签选择器  
```css
p{
    color:black;
}
```
2. 类选择器
```html
<p class='p'>多个类的话用空格隔开 </p>

.p{
    color:black
}
```
3. id选择器
```css
#one{
    color:red;
}

<p id='one'>id选择器只能是一对一的关系</p>
```
### 复杂选择器
1. 复合选择器  
```css
p.aaa{
    作用于p标签里的aaa类
}
```
2. 组合选择器
```css
h1,p,.aaa{

}
```
3. 嵌套选择器  
```css
div p{
    .div .p等标签,类,id都可以生效
    作用于div里面的p,子级和孙级等后代级都起作用
    css3中div>p,只有子级才会生效
    空格不区分上下级,>区分上下级
}
```
### 其他选择器
1. 伪类选择器
```css
        一般用于连接,别的标签也可以使用
            a:link{   未访问
                color:cyan
            }
            a:hover{ 悬浮
                color: cornflowerblue;
            }
            a:active{ 点击中
                color: crimson;
            }
            a:visited{ 点击后
                color: darkgray;
            }
```

## 选择器优先级

1. 优先级
    1. 行内样式>ID选择器>类选择器>标签选择器  
        原因:首先加载标签选择器,后加载的会覆盖先加载的样式  
2. 内外部样式加载顺序   
    就近原则,后加载的会覆盖先加载的样式
3. !important  
    拥有最高优先级  
    用法是在样式后面加!important.  

## 属性  
所有css属性的默认值都是inherit(继承自父类,也就是上级标签)
### 字体属性
       html根元素字体默认大小为16px,
        为了方便计算,一般先上来就把body的字体设为62.5%. 
        也就是把body的字体设为10px.
1. font-size:20px;字体像素大小.  
        font-size:50%; 相对父标签的50%
        font-size:2em;父标签的2倍  
2. font-weight:   字体的粗细
         取值:normal 普通  
                   bold   粗体
                   数值    normal==400        bold==700,可以自己用数值设置粗细
                font-weight:500;
3. font-family:    设置字体  
    一般设置3种字体:font-family:华文行楷,楷体,arial;  
    当当前系统没有前面的字体时,会用后面的字体,arial字体是都会有的.
4. font-style: 字体样式
    取值:normal  普通的字体  
                italic    斜体  
5.  font:  简写样式  
        顺序:样式-->粗细-->大小-->设置字体
        font:normal bold 20px 华为楷体,楷体,arial 
