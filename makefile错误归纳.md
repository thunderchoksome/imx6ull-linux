+ 提示obj/xxx.s不匹配目标模式时错误可能为$(SFILENDIRS:.s=.o)这里.s或者.o前面不能有留空格!!
+ makefile error：56 ：***遗漏分隔符，停止.提示：在makefile文件中某一行（这里为56行），少了一个分隔符，故编译停止。解决：在编写makefile文件时，编写规则规定所有的命令（包括自定义工具名打头的命令），如gcc，clean，all等，之前必须是tab作为分隔符，不能用空格代之。因为tab通常为4个空格的长度。所以将错误行Backspace到最左边，再加一tab键开始即可了。
+ makefile error：***/arch:是一个目录，停止。
提示：makefile文件中某一参数或者路径为一个目录，故make工具不能识别该参数，继而停止工作。
解决：这一问题在makefile的所有错误中最为隐蔽，不易检查，却十分容易犯。在makefile中所有路径的引用或定义行末都不能有空格，应直接以回车符结束。
例如：ROOTDIR = /home/my_nios2/uClinux-dist<space>
这样的一个路径定义在make过程中就会报上面的错误，去掉行末的空格键（<sapce>）改为如下即可。
ROOTDIR = /home/my_nios2/uClinux-dist