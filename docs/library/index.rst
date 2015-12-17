MicroPython 类库
=====================

MicroPython库
-------------------------
具体实现见以下描述

.. toctree::
   :maxdepth: 1

   micropython.rst

Python标准库
-------------------------

以下是内置Python标准库
附加库请查看 `micropython-lib repository
<https://github.com/micropython/micropython-lib>`_.

.. only:: port_unix

    .. toctree::
       :maxdepth: 1
    
       cmath.rst
       gc.rst
       math.rst
       os.rst
       struct.rst
       sys.rst
       time.rst

.. only:: port_pyboard

    .. toctree::
       :maxdepth: 1
    
       cmath.rst
       gc.rst
       math.rst
       os.rst
       select.rst
       struct.rst
       sys.rst
       time.rst

.. only:: port_wipy

    .. toctree::
       :maxdepth: 1
    
       gc.rst
       os.rst
       select.rst
       sys.rst
       time.rst

Python 微型库
----------------------

以下是专为micropython设计的微型库以替代标准库

.. only:: not port_unix

    微型库可以被重写。例如自带模块json，当import json时，系统会先寻找json.py，
    然后尝试需找目录json，最后才寻找json包，如果什么都没找到则启用该微型库ujson。

.. only:: port_pyboard or port_unix

   .. toctree::
      :maxdepth: 1
    
      ubinascii.rst
      uctypes.rst
      uhashlib.rst
      uheapq.rst
      ujson.rst
      ure.rst
      usocket.rst
      uzlib.rst

.. only:: port_pyboard

   Pyboard特定函数
   ---------------------------------

   .. toctree::
      :maxdepth: 2

      pyb.rst
      network.rst

.. only:: port_wipy

   .. toctree::
      :maxdepth: 1

      ubinascii.rst
      ujson.rst
      ure.rst
      usocket.rst
      ussl.rst

.. only:: port_wipy

   Libraries specific to the WiPy
   ---------------------------------

   The following libraries are specific to the WiPy.

   .. toctree::
      :maxdepth: 2

      machine.rst
      network.rst
      wipy.rst


.. only:: port_esp8266

   Libraries specific to the ESP8266
   ---------------------------------

   The following libraries are specific to the ESP8266.

   .. toctree::
      :maxdepth: 2

      pyb.rst
      esp.rst
      network.rst
