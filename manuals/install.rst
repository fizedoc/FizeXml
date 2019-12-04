========
安装说明
========

FizeXml 的环境要求如下：

-  "php": ">=5.4.0"
-  如果使用 Dom ，请开启 dom 扩展
-  如果使用 LibXml ，请开启 libxml 扩展
-  如果使用 Rss ，请开启 dom 扩展
-  如果使用 SimpleXml ，请开启 simplexml 扩展
-  如果使用 Wddx ，请开启 wddx 扩展
-  如果使用 Xml ，请开启 xml 扩展
-  如果使用 XmlRpc ，请开启 xmlrpc 扩展


使用Composer安装
================

FizeXml 支持使用 `Composer <https://www.phpcomposer.com/>`_ 安装，也是唯一官方推荐的安装方法。

.. note::

   如果您尚未安装 composer ，请参考 `安装 composer <https://docs.phpcomposer.com/00-intro.html>`_ 。
   
   使用 `阿里云镜像 <https://developer.aliyun.com/composer>`_ 以提高下载速度及稳定性。


在命令行下面，切换到您的项目根目录下面并执行下面的命令：

.. code-block:: bash

  composer require fize/xml
  
好了！一步到位，您现在可以开始使用 FizeXml 了，就是这么简单！~

.. note::

   Fize 项目(包括所有子项目)严格遵守 `语义化版本 <https://semver.org/lang/zh-CN/spec/v2.0.0.html>`_ ，您可以放心大胆的使用。