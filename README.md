学习Sass

Sass与less的区别

一. 安装ruby
  1. 下载路径
      https://rubyinstaller.org/downloads/
  2. 查看版本
      ruby -v
    
二. 安装sass
  1. 安装
      gem install sass
  2. 查看版本
      sass -v
  3. 更新
      gem update sass
  4. 卸载
      gem uninstall sass
      
三. 安装compass(可不安装)
  1. 安装
      gem install compass
  2. 查看版本
      compress -v
  
四. 编译sass
  1. 单文件转换(index.scss编译成index.css)
      sass index.scss index.css
  2. 单文件实时监听(index.scss编译成index.css)
      sass --watch index.scss:index.css
  3. 如果你有很多的sass文件的目录，你也可以告诉sass监听整个目录
      a. 监听sass文件夹下的index.scss文件编译到public文件夹下的	 index.css文件
          sass --watch sass/index.scc:public/index.css --style expanded
      b. 监听sass下的所有.scss文件编译到public文件夹下
          sass --watch sass/:public --style expanded
  4. 编译排版格式( 监听可以加上 --watch)   四种编译模式(输出风格)	
      a. 编辑之前的scss样式
      b. 嵌套式 nested 默认格式
      c. 展开式 expanded
      d. 紧凑式 compact
      e. 压缩式 compressed
      
五. 反编译
  1. 将fileName.css文件反编译成fileName.scss
      sass-convert index.css index.scss
  2. 将fileName.scss文件编译成fileName.sass格式
      sass-convert index.scss index.sass
      
六. 注释
  1. 单行注释，只保留在sass源文件中，编译后会被省略掉
      //不会出现在编译之后任何格式的CSS文件中。
  2. 多行注释，会保留到编译后的文件中
      /* 只会出现在编译之后代码格式为expanded的CSS文件中。 */
  3. 强制注释(重要注释)，即使压缩编译模式，也会保留注释，通常用于声明	 版权信息	
      /*!  会出现在任何代码格式的CSS文件中。  */	
      
七. 导入：sass中如导入其他sass文件，最后编译为一个css文件，	  优于纯css的@import	
  1. @import命令，用来插入外部文件，注意默认无后缀名时是引入.sass	或.scss文件。
      @import “themes/night-sky”
  2. 以下几种情况插入的是.css文件，则等同于css的import命令
      @import "url(.....)";    //被导入文件是一个URL地址形式给出的
  3. 和css中@import的区别
  
八. Mixin是可以重用的代码块
  1. @minxin基础用法
  2. @mixin传递参数
  3. @mixin 传递多值参数
  4. 向 @mixin 传递内容
  5. @mixin和@extend的区别：
  
九. 扩展/继承(@extend)

十. 自定义函数

十一. 颜色函数
  1. RGB	
  2. lighten()和darken()函数
  3. Ie-hex-str()函数	
  
十二. 流程控制语句	
  1. if判断	
  2. @for	
  3. @while	
  4. @each	
  
十三. 数据类型
