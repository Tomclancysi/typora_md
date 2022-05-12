---
layout: post
title: install gdal
---



# 安装gdal遇到py的坑

- python查找module的路径是按照sys.path的路径(是启动解释器时确定的，内容包含环境变量PYTHONPATH的值，site-package的值等等)
- os.environ实际上是所有环境变量的字典 包含了PATH
- 印象笔记python中说了 更换jupyter kernel

安装gdal等包，用whl安装 https://www.lfd.uci.edu/~gohlke/pythonlibs/#gdal  pip install ***.whl
