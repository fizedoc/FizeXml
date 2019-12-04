=============
XML 解析器
=============


+-------------+----------+
|属性         |值        |
+=============+==========+
|命名空间     |fize\\xml |
+-------------+----------+
|类名         |Xml       |
+-------------+----------+


:方法:


+-------------------------------------+------------------------------------------------------------+
|方法名                               |说明                                                        |
+=====================================+============================================================+
|`errorString()`_                     |根据给定的 code 获得 XML 解析器错误字符串。                 |
+-------------------------------------+------------------------------------------------------------+
|`getCurrentByteIndex()`_             |获取 XML 解析器的当前字节索引                               |
+-------------------------------------+------------------------------------------------------------+
|`getCurrentColumnNumber()`_          |获取 XML 解析器的当前列号                                   |
+-------------------------------------+------------------------------------------------------------+
|`getCurrentLineNumber()`_            |获取 XML 解析器的当前行号                                   |
+-------------------------------------+------------------------------------------------------------+
|`getErrorCode()`_                    |获取 XML 解析器错误代码                                     |
+-------------------------------------+------------------------------------------------------------+
|`parseIntoStruct()`_                 |将 XML 数据解析到数组中                                     |
+-------------------------------------+------------------------------------------------------------+
|`parse()`_                           |开始解析一个 XML 文档                                       |
+-------------------------------------+------------------------------------------------------------+
|`parserCreateNs()`_                  |生成一个支持命名空间的 XML 解析器                           |
+-------------------------------------+------------------------------------------------------------+
|`parserCreate()`_                    |建立一个 XML 解析器                                         |
+-------------------------------------+------------------------------------------------------------+
|`parserFree()`_                      |释放当前的 XML 解析器                                       |
+-------------------------------------+------------------------------------------------------------+
|`parserGetOption()`_                 |从 XML 解析器获取选项设置信息                               |
+-------------------------------------+------------------------------------------------------------+
|`parserSetOption()`_                 |为指定 XML 解析进行选项设置                                 |
+-------------------------------------+------------------------------------------------------------+
|`setCharacterDataHandler()`_         |建立字符数据处理器                                          |
+-------------------------------------+------------------------------------------------------------+
|`setDefaultHandler()`_               |建立默认处理器                                              |
+-------------------------------------+------------------------------------------------------------+
|`setElementHandler()`_               |建立起始和终止元素处理器                                    |
+-------------------------------------+------------------------------------------------------------+
|`setEndNamespaceDeclHandler()`_      |建立终止命名空间声明处理器                                  |
+-------------------------------------+------------------------------------------------------------+
|`setExternalEntityRefHandler()`_     |建立外部实体指向处理器                                      |
+-------------------------------------+------------------------------------------------------------+
|`setNotationDeclHandler()`_          |建立注释声明处理器                                          |
+-------------------------------------+------------------------------------------------------------+
|`setObject()`_                       |在对象中使用 XML 解析器                                     |
+-------------------------------------+------------------------------------------------------------+
|`setProcessingInstructionHandler()`_ |建立处理指令（PI）处理器                                    |
+-------------------------------------+------------------------------------------------------------+
|`setStartNamespaceDeclHandler()`_    |建立起始命名空间声明处理器                                  |
+-------------------------------------+------------------------------------------------------------+
|`setUnparsedEntityDeclHandler()`_    |建立未解析实体定义声明处理器                                |
+-------------------------------------+------------------------------------------------------------+


方法
======
errorString()
-------------
根据给定的 code 获得 XML 解析器错误字符串。

.. code-block:: php

  public static function errorString (
      int $code
  ) : string


:参数:
  +-------+--------------------------------------------------+
  |名称   |说明                                              |
  +=======+==================================================+
  |code   |由 xml_get_error_code() 返回的错误代码。          |
  +-------+--------------------------------------------------+
  
  


getCurrentByteIndex()
---------------------
获取 XML 解析器的当前字节索引

.. code-block:: php

  public function getCurrentByteIndex () : int



getCurrentColumnNumber()
------------------------
获取 XML 解析器的当前列号

.. code-block:: php

  public function getCurrentColumnNumber () : int



getCurrentLineNumber()
----------------------
获取 XML 解析器的当前行号

.. code-block:: php

  public function getCurrentLineNumber () : int



getErrorCode()
--------------
获取 XML 解析器错误代码

.. code-block:: php

  public function getErrorCode () : int



parseIntoStruct()
-----------------
将 XML 数据解析到数组中

.. code-block:: php

  public function parseIntoStruct (
      string $data,
      array &$values,
      array &$index = null
  ) : int


:参数:
  +-------+------------------------------------------------+
  |名称   |说明                                            |
  +=======+================================================+
  |data   |待解析数据                                      |
  +-------+------------------------------------------------+
  |values |指向 values 数组                                |
  +-------+------------------------------------------------+
  |index  |含有指向 values 数组中对应值的指针              |
  +-------+------------------------------------------------+
  
  

:返回值:
  失败返回 0，成功返回 1


parse()
-------
开始解析一个 XML 文档

.. code-block:: php

  public function parse (
      string $data,
      bool $is_final = false
  ) : int


:参数:
  +---------+----------------------------------------------+
  |名称     |说明                                          |
  +=========+==============================================+
  |data     |需要解析的数据集                              |
  +---------+----------------------------------------------+
  |is_final |是否为当前解析中最后一段数据。                |
  +---------+----------------------------------------------+
  
  

:返回值:
  成功时返回1，失败时返回0


parserCreateNs()
----------------
生成一个支持命名空间的 XML 解析器

.. code-block:: php

  public function parserCreateNs (
      string $encoding = null,
      string $separator = ":"
  ) : resource


:参数:
  +----------+-------------------------------------+
  |名称      |说明                                 |
  +==========+=====================================+
  |encoding  |指定解析后输出数据的编码             |
  +----------+-------------------------------------+
  |separator |命名空间和标签名的分隔符             |
  +----------+-------------------------------------+
  
  


parserCreate()
--------------
建立一个 XML 解析器

.. code-block:: php

  public function parserCreate (
      string $encoding = null
  ) : resource


:参数:
  +---------+-------------------------------------+
  |名称     |说明                                 |
  +=========+=====================================+
  |encoding |指定解析后输出数据的编码             |
  +---------+-------------------------------------+
  
  


parserFree()
------------
释放当前的 XML 解析器

.. code-block:: php

  public function parserFree () : bool


:返回值:
  成功返回true，失败返回false


parserGetOption()
-----------------
从 XML 解析器获取选项设置信息

.. code-block:: php

  public function parserGetOption (
      int $option
  ) : mixed


:参数:
  +-------+-------------------------------+
  |名称   |说明                           |
  +=======+===============================+
  |option |要获取的设置选项名称           |
  +-------+-------------------------------+
  
  

:返回值:
  如果失败返回false，同时产生E_WARNING警告


::

    参数 `$option` :
    可以使用 XML_OPTION_CASE_FOLDING 和 XML_OPTION_TARGET_ENCODING 常量。


parserSetOption()
-----------------
为指定 XML 解析进行选项设置

.. code-block:: php

  public function parserSetOption (
      int $option,
      mixed $value
  ) : bool


:参数:
  +-------+-------------------------------+
  |名称   |说明                           |
  +=======+===============================+
  |option |要设置的选项名称               |
  +-------+-------------------------------+
  |value  |要给选项设置的新值。           |
  +-------+-------------------------------+
  
  

:返回值:
  成功返回true，失败返回false


::

    参数 `$option` :
    可以使用 XML_OPTION_CASE_FOLDING、XML_OPTION_SKIP_TAGSTART、XML_OPTION_SKIP_WHITE、XML_OPTION_TARGET_ENCODING常量


setCharacterDataHandler()
-------------------------
建立字符数据处理器

.. code-block:: php

  public function setCharacterDataHandler (
      callable $handler
  ) : bool


:参数:
  +--------+-------------+
  |名称    |说明         |
  +========+=============+
  |handler |处理函数     |
  +--------+-------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$handler` :
    处理函数的定义必须为handler( resource $parser , string $data )


setDefaultHandler()
-------------------
建立默认处理器

.. code-block:: php

  public function setDefaultHandler (
      callable $handler
  ) : bool


:参数:
  +--------+-------------+
  |名称    |说明         |
  +========+=============+
  |handler |处理函数     |
  +--------+-------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$handler` :
    处理函数的定义必须为handler( resource $parser , string $data )


setElementHandler()
-------------------
建立起始和终止元素处理器

.. code-block:: php

  public function setElementHandler (
      callable $start_element_handler,
      callable $end_element_handler
  ) : bool


:参数:
  +----------------------+----------------------+
  |名称                  |说明                  |
  +======================+======================+
  |start_element_handler |起始元素处理器        |
  +----------------------+----------------------+
  |end_element_handler   |终止元素处理器        |
  +----------------------+----------------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$start_element_handler` :
      定义必须为start_element_handler ( resource $parser , string $name , array $attribs )
    参数 `$end_element_handler` :
      定义必须为end_element_handler ( resource $parser , string $name )


setEndNamespaceDeclHandler()
----------------------------
建立终止命名空间声明处理器

.. code-block:: php

  public function setEndNamespaceDeclHandler (
      callable $handler
  ) : bool


:参数:
  +--------+----------------+
  |名称    |说明            |
  +========+================+
  |handler |处理器函数      |
  +--------+----------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$handler` :
    处理器函数必须为handler ( resource $parser , string $prefix )


setExternalEntityRefHandler()
-----------------------------
建立外部实体指向处理器

.. code-block:: php

  public function setExternalEntityRefHandler (
      callable $handler
  ) : bool


:参数:
  +--------+----------------+
  |名称    |说明            |
  +========+================+
  |handler |处理器函数      |
  +--------+----------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$handler` :
    处理器函数必须为handler ( resource $parser , string $open_entity_names , string $base , string $system_id , string $public_id )


setNotationDeclHandler()
------------------------
建立注释声明处理器

.. code-block:: php

  public function setNotationDeclHandler (
      callable $handler
  ) : bool


:参数:
  +--------+----------------+
  |名称    |说明            |
  +========+================+
  |handler |处理器函数      |
  +--------+----------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$handler` :
    处理器函数必须为handler ( resource $parser , string $notation_name , string $base , string $system_id , string $public_id )


setObject()
-----------
在对象中使用 XML 解析器

.. code-block:: php

  public function setObject (
      object &$object
  ) : bool


:参数:
  +-------+-----------------------------------------------------------------+
  |名称   |说明                                                             |
  +=======+=================================================================+
  |object |使得 parser 指定的解析器可以被用在 object 对象中                 |
  +-------+-----------------------------------------------------------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


setProcessingInstructionHandler()
---------------------------------
建立处理指令（PI）处理器

.. code-block:: php

  public function setProcessingInstructionHandler (
      callable $handler
  ) : bool


:参数:
  +--------+----------------+
  |名称    |说明            |
  +========+================+
  |handler |处理器函数      |
  +--------+----------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$handler` :
    处理器函数必须为handler( resource $parser , string $target , string $data )


setStartNamespaceDeclHandler()
------------------------------
建立起始命名空间声明处理器

.. code-block:: php

  public function setStartNamespaceDeclHandler (
      callable $handler
  ) : bool


:参数:
  +--------+----------------+
  |名称    |说明            |
  +========+================+
  |handler |处理器函数      |
  +--------+----------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$handler` :
    处理器函数必须为handler( resource $parser , string $prefix , string $uri )


setUnparsedEntityDeclHandler()
------------------------------
建立未解析实体定义声明处理器

.. code-block:: php

  public function setUnparsedEntityDeclHandler (
      callable $handler
  ) : bool


:参数:
  +--------+----------------+
  |名称    |说明            |
  +========+================+
  |handler |处理器函数      |
  +--------+----------------+
  
  

:返回值:
  成功时返回 TRUE， 或者在失败时返回 FALSE。


::

    参数 `$handler` :
    处理器函数必须为handler( resource $parser , string $entity_name , string $base , string $system_id , string $public_id , string $notation_name )


