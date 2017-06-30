# SYCacheFileViewController
缓存文件视图控制器


* 显示指定目录下的子目录及文件；
  * 子目录可以继续点击进入下级子目录，及显示下级文件；
  * 文件可以点击查看，根据不格式进行展示，如音频播放、视频播放、doc/excel/ppt/pdf/txt等打开；
* 目录与文件的删除操作



![SYCacheFileViewController.png](./images/SYCacheFileViewController.png)


# 效果图-目录与文件

![cacheFile_directory.gif](./images/cacheFile_directory.gif)

# 效果图-图片查看

![cacheFile_image.gif](./images/cacheFile_image.gif)

# 效果图-视频播放

![cacheFile_video.gif](./images/cacheFile_video.gif)

# 效果图-音频播放

![cacheFile_audio.gif](./images/cacheFile_audio.gif)

# 效果图-文档查看-word/excel/ppt/pdf

![cacheFile_File01.gif](./images/cacheFile_File01.gif)

# 效果图-文档查看：txt/htm/……

![cacheFile_File02.gif](./images/cacheFile_File02.gif)



# 使用示例
~~~ javascript

// 导入头文件
#import "SYCacheFileViewController.h"

~~~

~~~ javascript

// 实例化 使用默认路径home
SYCacheFileViewController *cacheVC = [[SYCacheFileViewController alloc] init];
[self.navigationController pushViewController:cacheVC animated:YES];

~~~

~~~ javascript

// 实例化 自定义目录、标题
SYCacheFileViewController *cacheVC = [[SYCacheFileViewController alloc] init];
// 指定目录，或默认目录
NSString *path = [SYCacheFileManager documentDirectoryPath];
NSArray *array = [SYCacheFileManager fileModelsWithFilePath:path];
cacheVC.cacheArray = [NSMutableArray arrayWithArray:array];
// 其它属性设置
cacheVC.cacheTitle = @"我的缓存文件";
[self.navigationController pushViewController:cacheVC animated:YES];

~~~