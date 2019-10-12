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
            a:link{   未访问时
                color:cyan
            }
            a:hover{ 悬浮时
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

### 文本属性  
1. color:文本颜色;  
    取值: 四种.  
    1. 颜色名;  
    2. #FFFFFF;16进制RGB,可缩写为3位,不区分大小写.    
    3. rgb(255,255,255);RGB函数.  
    4. rgba(255,255,255,alpha);alpha设置透明度,  
                    取值0(完全透明)到1(完全不透明)之间,可设置小数.  
2. line-height:50px;   
    设置行高,行与行之间的距离,单位px;  
3. text-align:center;  
    设置水平对齐方式,取值left,center,right(左中右).  
4. vertical-align:top;  
    设置图片和文字的垂直对齐方式.  
    取值:top,middle,bottom(上中下).  
5. text-indent:30px;  
    首行缩进  
6. text-decoration:overline;  
    文本缩进.  
    取值:underline,overline,line-through(下划线,上划线,删除线).   
7. text-transform:lowercase;  
    设置英文文本大小写.  
    取值:lowercase,uppercase,capitalize(全部小写,全部大写,全部单词的首字母大写).  
8. word-spacing: 0px;  
    单词间距
9. letter-spacing: 0px;  
    字符间距.  
10. white-space:nowrap;  
    文本超出后是否换行.  
    取值:wrap,nowrap(换行,不换行).  

### 背景属性
1. background-color:#ffffff;    
    背景颜色.取值rgb或者transparent(透明的,会显出下层颜色)
2. background-image:url(image/image.png)  
    背景图片(需要用url指定路径)  
    注意:外部引用background-image:url(../image/image.png)  
3. background-repeat: 
    背景图片重复方式.  
    取值:repeat(默认,x和y都重复),  
    repeat-x(水平重复),repeat-y(垂直重复),  
    no-repeat(不重复).  
4. background-position:10px 10px;  
    两种取值方式:  
    1. 关键字:top,bottom,left,right,center.    
            background-position:top center;
    2. 坐标:浏览器左上角为0.0 ,向右为x正方向,向左为y正方向.  
        background-position:10px 10px;  
    3. css雪碧图(css精灵)  
        ```css
        在一张集合了小图标的图片里显示图标,
        先指定显示的大小,再用背景定位.
                width:10px;
                height: 10px;
                background-position: 15px 25px;
        ```
5. background-attachment: scroll;  
    图片是否跟随滚动条滚动.  
    取值:scroll(默认,滚动),fixed(固定).  
6. background:      
    简写,没有顺序要求.

### 列表属性
1. 



























