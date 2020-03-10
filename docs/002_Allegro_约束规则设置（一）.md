#   Allegro 约束规则设置(一)

##  一、基本约束规则设置

### 1.1 线间距设置

####    1.1.1 设置默认间距规则

*   点击 CM  图标，打开约束管理器

<img src="images/0201.png" width="100%">

<img src="images/0202.png" width="100%">

*   单击 Spacing，再点击All Layers，如下图所示。右边有一个DEFAULT 就是默认规则，我们可以修改其值 。

<img src="images/0203.png" width="100%">

*   按住Shift 键，点击第一个和最后一个即可选中所示，然后输入一个值，这样就都修改了，如下图所示

<img src="images/0204.png" width="100%">

#### 1.1.2 定义特殊的间距约束

*   点选Default按鼠标右键，执行Create-Spacing CSet ， 加入新规则。取一个有意义点的名字，如下图所示，单击OK 

<img src="images/0205.png" width="100%">

其值是从默认规则拷贝的，先修改其值。按住Shift 键选中所有，输入12，回车。

<img src="images/0206.png" width="100%">

然后为所需要设置的网络分配规则
单击左边的Net-All Layers，在右边工作簿中，为GND 网络设置12MIL_SPACE 规则，在Referenced Spacing CSet 下选中12MIL_SPACE，如下图所示

<img src="images/0207.png" width="100%">

####    1.1.3 设置Class-Class规则

若针对不同的信号群组有不同的间距规则，则需要设置Class-Class
选到Net Class-Class 后，在右边CLOCK(2)上右键选择Ctreat-Class-Class...，选择2个不同的Net Classes，单击OK，如下图所示

<img src="images/0208.png" width="100%">

如下图所示。在右边的Referenced Spacing CSet 栏可以修改其值。

执行Analyze-Analysis Modes...，可以看到Spacing Mode的检查模式 

<img src="images/0209.png" width="100%">

### 1.2 线宽设置

####    1.2.1 设置默认线宽约束

*   点选Physical Constraint Set 即可出现Default 的Physical 相关设定值，如Line Width、Neck width..等

<img src="images/0210.png" width="100%">

####    1.2.2 设置特殊物理规则

点选Default按鼠标右键，执行Create Physical CSet 加入新规则，修改其值，如下图所示

<img src="images/0211.png" width="100%">

然后在分配网络，左边点击Net-All Layers，右边为所需设置的网络分配规则，如下图所示

<img src="images/0212.png" width="100%">

### 1.3 过孔设置

Physical Constraint Set 里面有一栏是Vias，点击即可设置，如下图所示

<img src="images/0213.png" width="100%">

点击默认规则的Vias，如下图所示

<img src="images/0214.png" width="100%">

Remove 可以移除过孔。在左边的过孔列表中双击即可添加

<img src="images/0215.png" width="100%">

同理，可设置其他物理规则的过孔

### 1.4 区域规则设置

Physical规则下，左边点击Region ，如下图所示

<img src="images/0216.png" width="100%">

在右边cds_2 右键并选择Create-Region...，输入规则名称 ，单击 OK ，然后输入其约束值 ，如下图所示

<img src="images/0217.png" width="100%">

然后执行Shape> Polygon/Rectangular/Circular 设定范围 。

<img src="images/0218.png" width="100%">

类选择为Constraint Region，子类为All。

Assign to Region分配的区域设置为刚才创建的RGN1.







