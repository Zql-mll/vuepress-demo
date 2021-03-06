### CSS规范

格式：

1. **缩进**：使用**tab**(**2**个空格)

2. **分号**：每个属性声明**末尾都要加分号**

   ```
   .element {
   	width: 20px;  // 添加分号
   }
   ```

3. **空格**：

   - 以下属性**不需要**空格：
     - 属性名后
     - !important 的 "!" 后
     - 行末不要有多余的空格
     - 属性值中"(" 后和 ")"前

   ```css
   .element {
   	background-color: rgba(0, 0, 0, .5);   // （ 前和 ）后不加空格
   }
   ```

   - 以下属性**需要**空格
     - 属性值前
     - 选择器 ">"，“+”，“~”前后
     - !important的 “!"前

4. **换行**

   - **不需要**换行：
     - "{"前
   - **需要**换行
     - "{" 后和"}"前
     - 每个属性独占一行
     - 多个规则的分隔符","后

   ```
   .element,    // 换行
   .dialog{
   	...
   }
   ```

5. **引号**

   - 最外层统一使用双引号
   - url的内容要用引号

6. **命名**

   - 类名使用小写字母，具体书写规范参照BEM规范

7. **属性声明顺序**

   - 相关的属性声明按右边的顺序做分组处理，组之间需要一个空行

   ```
   .element {
   	display:block;
   	float:right;
   	
   	position:absolute;
   	top:0;
   	right:30px;
   	z-index:10;
   	
   	border:1px solid #e5e5e5;
   	border-radius:3px;
   	width:100px;
   	height:100px;
   	
   	font: normal 13px "Helvetical Neue", sans-serif;
   	line-height:1.5;
   	text-align:center;
   	
   	color:#333;
   	background-color:#f5f5f5;
   	
   	opacity:1;
   }
   ```

   

8. **颜色**

   - 颜色16进制用小写字母

9. **媒体查询**

   - 尽量将媒体查询的规则开进与他们相关的规则，不要讲他们一起放在一个独立的样式文件夹中，或者丢在文档的最底部，这样做只会让大家以后给你更容易忘记他们

10. **杂项**

    - 去掉小数点前的0
    - 去掉数字中不必要的小数点和末尾的0
    - 属性值 0 后面不要加单位
    - 无前缀的标准属性应该写在有前缀的属性后面
    - 不要在同一规则里出现重复的属性，如果重复的属性是连续的则没有关系
    - 用border:0 来代替 border:none
    - 选择器不要超过4层（在scss中如果超过4层应该考虑用嵌套的方式来写，但是scss嵌套最多也不能超过4层）



书写方式**额外要求**(**必看**)：

1. **不**允许轻易**写行内样式**
2. **不**允许轻易**写important**，除非要覆盖UI框架的行内样式
3. **不**允许**写无意义的类名或id名**，例如：test1,name2
4. .尽量**少**使用**标签选择器**
5. **少用display:none**减少重绘
6. 组件样式设置scope