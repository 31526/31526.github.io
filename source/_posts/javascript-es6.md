title: javascript-es6
date: 2015-10-12 15:01:02
tags: [js, apache, es6]
categories: [javascript]
keywords: Javascript, NodeJS, ES6, ECMASCript6
description: ECMAScript是一种由Ecma国际（前身为欧洲计算机制造商协会,英文名称是European Computer Manufacturers Association）通过ECMA-262标准化的脚本程序设计语言
---


# 本书力争覆盖ES6与ES5的所有不同之处，对涉及的语法知识给予详细介绍，并给出大量简洁易懂的示例代码。

本书为中级难度，适合已有一定JavaScript语言基础的读者，用来了解这门语言的最新发展；也可当作参考手册，查寻新增的语法点。

全书第一版已由电子工业出版社于2014年10月出版（版权页，内页1，内页2），铜版纸全彩印刷，附有索引。目前，网站的内容是第二版的初稿，预订2016年年初出版。感谢张春雨编辑支持我将全书开源的做法。如果您对本书感兴趣，建议考虑购买纸版。这样可以使出版社不因出版开源书籍而亏钱，进而鼓励更多的作者开源自己的书籍。

<!-- more -->

# beijing-javascript-es6
## ES6
MySQLdb is an thread-compatible interface to the popular MySQL database server that provides the Python database API.


If you want to write applications which are portable across databases, use MySQLdb, and avoid using this module directly. _mysql provides an interface which mostly implements the MySQL C API. For more information, see the MySQL documentation. The documentation for this module is intentionally weak because you probably should use the higher-level MySQLdb module. If you really need it, use the standard MySQL docs and transliterate as necessary.


## ES5

The simplest possible database connection is:

```
import _mysql
db=_mysql.connect()
This creates a connection to the MySQL server running on the local machine using the standard UNIX socket (or named pipe on Windows), your login name (from the USER environment variable), no password, and does not USE a database. Chances are you need to supply more information.:
```

db=_mysql.connect("localhost","joebob","moonpie","thangs")
This creates a connection to the MySQL server running on the local machine via a UNIX socket (or named pipe), the user name "joebob", the password "moonpie", and selects the initial database "thangs".

We haven't even begun to touch upon all the parameters connect() can take. For this reason, I prefer to use keyword parameters:

```
db=_mysql.connect(host="localhost",user="joebob",
                  passwd="moonpie",db="thangs")
```
This does exactly what the last example did, but is arguably easier to read. But since the default host is "localhost", and if your login name really was "joebob", you could shorten it to this:

### dodolook
The MySQL C API has been wrapped in an object-oriented way. The only MySQL data structures which are implemented are the MYSQL (database connection handle) and MYSQL_RES (result handle) types. In general, any function which takes MYSQL *mysql as an argument is now a method of the connection object, and any function which takes MYSQL_RES *result as an argument is a method of the result object. Functions requiring none of the MySQL data structures are implemented as functions in the module. Functions requiring one of the other MySQL data structures are generally not implemented. Deprecated functions are not implemented. In all cases, the mysql_ prefix is dropped from the name. Most of the conn methods listed are also available as MySQLdb Connection object methods. Their use is non-portable.



### welcome


Integer constant stating the level of thread safety the interface supports. This is set to 1, which means: Threads may share the module.

#### COMMIT or ROLLBACK
The MySQL protocol can not handle multiple threads using the same connection at once. Some earlier versions of MySQLdb utilized locking to achieve a threadsafety of 2. While this is not terribly hard to accomplish using the standard Cursor class (which uses mysql_store_result()), it is complicated by SSCursor (which uses mysql_use_result(); with the latter you must ensure all the rows have been read before another query can be executed. It is further complicated by the addition of transactions, since transactions start when a cursor execute a query, but end when COMMIT or ROLLBACK is executed by the Connection object. Two threads simply cannot share a connection while a transaction is in progress, in addition to not being able to share it during query execution. This excessively complicated the code to the point where it just isn't worth it.

#### The general upshot of this is: 
Don't share connections between threads. It's really not worth your effort or mine, and in the end, will probably hurt performance, since the MySQL server runs a separate thread for each connection. You can certainly do things like cache connections in a pool, and give those connections to one thread at a time. If you let two threads use a connection simultaneously, the MySQL client library will probably upchuck and die. You have been warned.

For threaded applications, try using a connection pool. This can be done using the Pool module.


## Objects Connection objects are returned by the connect() function.

commit()
If the database and the tables support transactions, this commits the current transaction; otherwise this method successfully does nothing.
rollback()
If the database and tables support transactions, this rolls back (cancels) the current transaction; otherwise a NotSupportedError is raised.
cursor([cursorclass])
### MySQL does not support cursors; however, 
cursors are easily emulated. You can supply an alternative cursor class as an optional parameter.
#### If this is not present, 

it defaults to the value given when creating the connection object, or the standard Cursor class. Also see the additional supplied cursor classes in the usage section.

#### There are many more methods defined on the connection object which are MySQL-specific. For more information on them, consult the internal documentation using pydoc.