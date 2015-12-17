开始运行你的第一个程序
======================

So简单，我们开始写入程序并且运行之

连接pyboard
-----------------------

连接USB，支持Mac、Win、Linux。只有一根线，你肯定不会接错。。

.. image:: img/pyboard_usb_micro.jpg

正常连接后，电源打开程序启动，绿灯亮半秒左右，绿灯灭表示启动完成。

打开pyboard的usb驱动
-----------------------------

电脑识别出usb后：

  - **Windows**: 像U盘一样打开一个存储器。

  - **Mac**: 桌面会出现一个可移动磁盘叫 NONAME

  - **Linux**: 发行版不同，显示不同。Ubuntu会和windows一样弹出，其它不会自动的，手动挂载之。
    输入 ``lsblk`` 看连接是否正常，然后 ``mount /dev/sdb1`` 其中sdb1是你在上步命令中查看到的sdb号

好了，现在已经连接上Pyboard的U盘。

U盘中有4个文件在 ``/flash`` 中

* `boot.py <http://micropython.org/resources/fresh-pyboard/boot.py>`_ -- 此文件首先启动，包含配置信息。

* `main.py <http://micropython.org/resources/fresh-pyboard/main.py>`_ -- 在boot.py启动后启动，个人程序放在这里。

* `README.txt <http://micropython.org/resources/fresh-pyboard/README.txt>`_ -- 简介，可删除

* `pybcdc.inf <http://micropython.org/resources/fresh-pyboard/pybcdc.inf>`_ -- windows下的u盘驱动，删除就sb了。mac删除不影响。

编辑 ``main.py``
-------------------

现在开始我们的自由编程，打开 ``main.py`` ，#号是注释

我们来通过代码点亮第4个led灯::

    # main.py -- put your code here!
    import pyb
    pyb.LED(4).on()

卧槽，简单的我都不想翻译了。。

运行你的程序
---------------------

要想运行程序，首先要温柔的 ``正常退出`` USB设备。不要粗暴的直接插拔哦。。

按下重置键（右边那个），按键后绿灯快闪，然后蓝灯亮起。程序已经运行。

