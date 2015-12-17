MicroPython 中文文档
=========================

在线：
http://micropython.popfeng.com/pyboard

生成本地文档
------------

安装 Sphinx

     pip install sphinx

在目录 `micropython/docs` 执行

    make MICROPY_PORT=<port_name> BUILDDIR=build/<port_name> html

`<port_name>` 可选值 `unix` `pyboard` `wipy` `esp8266`

最终文档生成在 `micropython/docs/build/<port_name>/html/index.html`.
