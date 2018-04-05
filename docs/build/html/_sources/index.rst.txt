.. Ccxgetaddr documentation master file, created by
   sphinx-quickstart on Wed Apr  4 14:38:33 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Ccxgetaddr's documentation!
======================================

中诚信征信数据研究部 依据手机号前7位和身份证号码匹配地址信息


.. toctree::
   :maxdepth: 2
   :caption: Contents:

API
===
API文档

.. toctree::
   :maxdepth: 4

   CcxgetaddrTools

Install
=======

.. code-block:: python

    cd package path
    python setup.py install


Example
======

.. code-block:: python

   import pandas as pd
   # 1.含有idno和mobile列的数据集
   df = read_csv(r'FILE_PATH') # 其中含有idno  mobile列
   f_Get_idno_Info(df.head(100)) # 获取身份证相关的地址信息和年龄性别信息
   f_Get_mobile_Info(df.head(100)) # 获取手机号码相关的信息

   # 2.列名不为idno或mobile
   df = read_csv(r'FILE_PATH') # 其中不含有idno  mobile列 其代表身份证的列名为id_no 代码手机号的为phone
   f_Get_idno_Info(df.id_no.head(100)) # 获取身份证相关的地址信息和年龄性别信息
   f_Get_mobile_Info(df.phone.head(100)) # 获取手机号码相关的信息
   #匹配完后 需要和原数据集merge


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
