# androidBsdiffUpdate

大家好。我是brok1n

这是我基于bsdiff二进制差分库修改而成的安卓客户端增量更新工具。

用这个工具。可以实现Bsdiff二进制差分工具的 差分包和旧版本文件合并成新版本文件的工作。

bsdiff是一个二进制差分工具。可以比较两个文件之间的差异。生成一个补丁文件。
使用这个补丁文件和一个文件。可以生成另一个文件。说的有点绕口了。 
bsdiff这个工具具体介绍大家可以在网上找找

简单来说。在安卓版本更新中。可以使用这个增量更新。减小软件更新时需要下载的数据

在安卓版本更新中的运用是
首先有一个旧版本Apk 和一个 新版本Apk 使用bsdiff的差分工具。可以检测出这两个文件的不同之处。
差分工具可以把这个不同之处。写入一个文件中。这个文件就是补丁文件 或者叫 补丁包

我们客户端装了一个旧版旧版本程序 当需要发布新版本时。将旧版本Apk文件和新版本apk文件做差分处理。
生成补丁包  将 补丁包 上传到服务器。 客户端需要更新时。只需要下载这个补丁包，下载到本地后。
使用bsdiff差分库的 patch 合并功能。将补丁包和旧版本Apk文件。生成新版本的apk文件。
这个生成出来的新版本apk文件和要发布的新版本apk文件是一样的。

使用上面这种流程。我们客户端在检测到新版本时，就直接下载补丁包就可以了。

这个生成的补丁包。在常规的版本升级中。补丁包会比新版本apk文件小很多。 
这样。客户端就可以减少下载的数据。加快版本更新下载，减少等待时间。减少手机使用的流量。

我这个项目。就是把bsdiff的 patch 合并工具 拆分出来。放在安卓程序里使用。

我这里是用ndk在eclipse下编译的。项目里有编译好的so文件。大家可以直接使用。

项目里也有个activity 简单的写了一下怎么使用这个 patch 合并工具 

大家也可以看看我的csdn博客。我会在博客里。讲一下这个大概的用法。我的博客地址
http://blog.csdn.net/brok1n/article/details/50406774

顺便我也把我写的demo放上来。大家稍作参考。

我的邮箱: 452700765@qq.com




