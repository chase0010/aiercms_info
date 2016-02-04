#AIER_CMS开发规则 <CSS样式部分>

#不允许模块CSS文件直接设置任何HTML元素样式，只能设置其Class和ID样式。
例：不直接定义 h1 div span form table 样式，而定义其Class或ID名 .good_list #goods .good_title 样式。

#在JSX文件中 className 和 id 均不能直接使用其名称，均用 style.class 或 style.id 替代。
例：错误用法  className="good_list" 或 id="goods"。
    正确用法  className={style.good_list} 或 id={style.goods}。

##定义多个class 
 className={style.classA + ' ' + style.classB + ' ' + style.classC}
 
