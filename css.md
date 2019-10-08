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
## 基本选择器
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
## 复杂选择器
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
## 其他选择器
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