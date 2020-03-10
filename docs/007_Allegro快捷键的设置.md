#   Allegro 快捷键的设置

Allegro可以通过修改env文件来设置快捷键，这对从其它软件如AD或PADS迁移过来的用户来说，可以沿用以前的操作习惯，还是很有意义的。

##  一、变量设置文件的路径

Allegro的变量文件一共有2个：一个是用户变量，一个是全局变量。

查找用户变量文件的位置，可以打开Allegro，在命令窗口里输入：echo$localenv（中间没有空格）

如果没有在系统属性里设置首页变量的路径，对于全局变量的位置，固定为软件安装目录内，比如我的就是：C:\Cadence\SPB_17.4\share\pcb\text内

通常建议修改用户变量env文件，而不要修改全局变量env文件

快捷键环境变量分为两种，即系统环境变量和用户环境变量，系统环境变量是全局性的，环境变量保存在Cadence的软件安装路径下，而环境用户变量的优先级高于系统-环境变量，即用户自定义的环境变量会覆盖掉系统的环境变量设置。我们应该在用户环境变量中进行快捷键的设置，这样有几个好处，不破坏系统的配置文件，每个用户可以自定义自己的习惯快捷键，而且可以将配置文件保存到U盘或者网盘，随身带走，了到新的计算机环境重新指向自己的环境变量文件可以，很是方便。

##  二、变量定义的方式

Cadence 系统是一个比较开放的系统，它给用户留了比较多的定制空间。在Allegro 中我们可以用alias 或funckey 命令来定义一个快捷键，以代替常用的设计命令。要使 定义的快捷键产生作用，我们有两种方式来定义：

### 2.1 命令窗口中定义

在命令窗口直接定义，但这样定义的快捷键只能在当前设计中使用，如果重新 启动设计时，快捷键将会失效。命令格式如下：

alias shortkey Keyboard Commands

funckey shortkey Keyboard Commands

1）如果直接键入alias 或funckey 命令然后回车，系统将会弹出所有快捷键列表，这相当于执行Tools->Utilities->Aliases/Function keys命令。

2）alias 命令不能用来定义字母，原因是字母键要用来输入命令行。但是funckey 命令 可以用来定义单个字母为快捷键，它比alias 命令更为强大，alias 能定义的它都能定义,但是字母 被定义成某快捷键后，该字母就不能用来输入键盘命令了。

3 ） Allegro 中的所有键盘命令(Keyboard Commands) 列表可以通过执行 Tools->Utilities->Keyboard Commands 命令来查看,这些命令都可以设置成快捷键。

### 2.2 本地环境中定义

在本地环境变量文件中直接定义，这样定义的命令将长期有效。本地的环境变量文件是evn 文件（D:/SPB_Data/pcbenv），我们可以对它进行编辑。我们的alias 命令可以在第二行开始写
（第一行是：source $TELENV），例如我们以前在Protel 或PowerPCB 中常 用的放大、缩小
命令就可以如下定义：

alias Pgdown zoom out

alias Pgup zoom in

另外我们经常用alias 命令来定义以下几个常用的shortkey:

alias ~R angle 90(旋转90 度)

alias ~F mirror(激活镜相命令)

alias ~Z next(执行下一步命令)

alias End redisplay（刷新屏幕）

alias Del Delete（激活删除命令）

alias Home Zoom fit（全屏显示）

alias Insert Define grid(设置栅格)

##  三、常用的命令 

### 3.1 常用键盘命令
在allegro 中有很多键盘命令，它是通过键盘输入来激活或执行相关的命令。键盘 命令基本上包含了大部分的菜单命令。下面列举几个常用的键盘命令。  

x 100：Y 坐标不变，X 方向移动100 个单位值（以设定的原点为参考点）  

y 100：X 坐标不变，Y 方向移动100 个单位值  

x 100 100：移动到（100，100）坐标处

pick 命令与上面的x 或y 命令功能相同，只是在执行pick 命令时会弹出一个窗口，输入想要的 坐标值就可以，与上面相对应，pick 命令也提供三种模式：pick、pickx 和picky。

mirror：激活镜相命令（本命令是先激活，后选择要镜相的对象）

rotate：激活旋转命令（本操作要先选取对象，后执行该命令）

angle 90：旋转90 度（本操作要先选取对象，后执行该命令）

### 3.2 常用快捷键

alias F2 done：结束当前命令

alias F3 oops：取消前一次操作

alias F4 cancel：取消当前命令

alias F5 show element：激活"属性显示"命令

alias F6 add connect：执行布线命令

alias F7 vertex：激活"增加倒角"命令

alias F8 zoom points：点取放大

alias F9 zoom fit：满屏显示

alias F10 zoom in：放大窗口

alias F11 zoom out：缩小窗口

alias F12 property edit：激活"属性编辑"命令

funckey + subclass -+：切换到下一层

funckey - subclass --：切换到上一层
