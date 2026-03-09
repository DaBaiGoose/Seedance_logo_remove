# Seedance AI视频去水印 云服务器版免费试用

随着最近 Seedance2 的爆火，对 AI 视频做去水印和高清修复的需求增多，本项目利用 DiffuEraser 模型来实现擦除指定位置水印，还配备上了最新的高清修复模型 FlashVSR ，可以在云GPU 上处理大量 AI 视频。目前内置有豆包16:9、豆包9:16、即梦16:9、即梦9:16、小云雀9:16、小云雀16:9、随变9:16 尺寸的视频去水印工作流，其他尺寸的任意静态水印也都可以自定义去除。

以下链接可以免实名注册并送算力点试用 GPU 服务器 to free use：

注册链接：https://growthdata.virtaicloud.com/t/xK

登陆后进入项目链接：

https://open.virtaicloud.com/web/project/detail/685505193227837440

![图10](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/10.png)

点击右上角运行一下，确定克隆项目和数据到自己工作空间，点击立即运行，启动开发环境后点右上角进入开发环境。

双击打开左侧的 项目说明.ipynb 文件，找到 “二、使用说明：” 下方的 !bash start.sh 这一行命令，点击选中后再点击上面的运行图标运行该命令行，即可启动服务界面：

![图11](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/11.png)

启动不到半分钟，出现如下 Running on local URL: http://0.0.0.0:8188 ，表示启动完成，按下图添加端口 8188 并将外部链接复制到浏览器新窗口打开，就可以打开 ComfyUI 界面使用去水印工作流啦。

![图12](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/12.png)

进入 ComfyUI 界面后，打开左侧栏目中的工作流，根据自己的视频来源（豆包/即梦/小云雀/随变）和尺寸（9:16还是16:9），双击打开对应的工作流.json 文件。然后在工作流最左侧的 Load Video 节点框中点击 choose video to upload 上传视频，然后点击右上方蓝色的 运行按钮即可开始运行。AI 生成的 16:9 或 9:16 视频差不多都是1280x704分辨率，且都不超过15s，按默认好的配置来 24G 显存+64G 内存足够了，总共耗时 8~12min 左右，默认可以高清放大到 1920x1024分辨率。

![图1](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/1.png)

内置的即梦或小云雀视频去水印工作流，需要按如图 Note 里的视频来源和规格，把对应的序号填到下面的 Int 单元格再开始运行。运行开始后，可以看到右上方显示的活跃任务的进度。

![图2](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/2.png)

任务完成后，打开左侧栏目中的资产，即可找到刚才工作流生成的结果，点开视频右下角，可以下载去水印和高清放大后的视频。

![图3](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/3.png)

![图4](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/4.png)

关闭高清放大(可选)

如果需要关闭上述工作流中的高清放大功能，可以参考下图设置，带高清放大的工作流会先把去水印的视频缩放到长边为 960 像素，再放大两倍变成 1920 像素，否则 24G 显存会不够用（懂行的也可以换平台更高的显卡配置）。关闭高清放大后，则可以调整去水印后的尺寸到原来的 1280 像素。

![图8](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/8.png)

去水印前：

![图5](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/5.png)

去水印后：

![图6](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/6.png)

高清放大：

![图7](https://github.com/DaBaiGoose/Seedance_logo_remove/blob/main/7.png)

最后用完记得点项目右上角停止和销毁来关闭服务器，以节省算力，也可以多注册几个号试用。

以上工作流和资源均来自互联网搬运，仅供学习研究使用，如果遇到 bug 或者对 AIGC 创作技术感兴趣的话，欢迎在项目说明.ipynb后面的群里反馈讨论。
