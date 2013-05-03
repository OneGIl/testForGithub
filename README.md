##浏览器在文件列表中产生的2个后退问题和1个衍生问题
* 系统:`XP SP3`![](http://)
* 浏览器:`IE8,谷歌26,火狐20`  
__以下问题重现当中会一直使用[oschina/git-osc](http://git.oschina.net/oschina/git-osc)这个仓库,其他仓库也有同样的问题__


##点击文件名情况下的后退问题:

当进入仓库后,点击文件列表当中的"readme.md"进入源代码页面,这个时候选择后退,浏览器中的地址栏上的URL已经变化了,但页面并没有得到更新.再选择后退的话,则会打开之前进入该仓库之前的页面.
当前的情况下如果要避免该问题就需要多点击一次鼠标,就是点击文件列表上面的仓库名(也就是"git-osc",如果点击页面顶部的"schina/git-osc"那么问题依然存在)

##点击仓库名产生的问题:

上面的问题中提到一个算是解决方法的方法,但这种方法下依然会有其他问题产生,就是当连续点击2次以上文件列表上的仓库名的时候,文件列表将不会显示,而只会出现文件列表从右到左滑动的效果.

##点击文件列表中提交者后产生的后退问题:

当进入仓库后,点击文件列表"readme.md"右侧的提交者名字后,会进入该提交者的页面,但在这个过程中,URL有会一个该文件的地址(例如:***/oschina/git-osc/blob/master/readme.md)一闪而过,然后才进入该提交者的主页上,这样就导致在提交者的主页上后退的时候会进入之前的文件源代码页面而非文件列表页面.
这个问题有一个特例,就是当某个提交者没有在网站上注册账号的情况下,该问题就不会出现,后退的时候就显示正常.(比如[oschina / android-app](http://git.oschina.net/oschina/android-app)这个仓库上的提交者)