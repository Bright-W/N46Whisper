# 常见问题说明

## 为什么使用N46Whisper？
用做饭打比方，N46Whisper为你提供了预制菜，不用从杀猪做起了。当然了，应用场景并非万能， 但根据目前收到的反馈，此应用确实可以在不同程度上让制作字幕的过程变得更轻松。

此应用也是希望提供一种思路来抛砖引玉。有能力的朋友，自然欢迎直接在源码基础上开发更完善的应用。

## 为什么使用Colab，没有更简单的用户界面或者可以下载使用的程序吗？
简单来说，使用Colab主要为了白嫖Google的GPU算力。官方建议若用利用large模型至少需要10G显存，大部分人的电脑是不可能有这个标准的配置的。此外，使用GPU可缩短处理时长到只需视频时长的三分之一左右，而如果在没有足够GPU配置的电脑上只能使用CPU处理，时间至少需要视频时长的三倍，反而得不偿失。

## 我打开了Colab，但还是不清楚如何使用，有没有更详细的教程？
请顺次点击各单元格最左端的“运行“图标，执行各单元格即可。

对于第一次接触Colab的朋友，即使在B站也可以找到很多教程，比如[这个](https://www.bilibili.com/video/BV13K4y1P7dx)，或者[这个](https://www.bilibili.com/video/BV1kd4y1g7Tq)。

用户贡献的对本应用的教程：

221231更新：B站的八次方巧克力同学制作了一份手把手的教程（虽然基于谷歌盘功能更新前的版本），但可以说是非常友好了。感谢！请移步[这里](https://www.bilibili.com/video/BV1cG4y1t7do)

230110更新：B站的西沢なぎさ同学制作的针对包含谷歌盘更新的教程。感谢！请移步[这里](https://www.bilibili.com/read/cv21090453)

## 能不能直接生成翻译，这样直接产出中文字幕文件，只需要压制了。
~今后会计划集成deepl的翻译，同时生成日语字幕和对应的中文字幕文件。~
目前已经集成了chatGPT的翻译功能，可以生成一个单独的双语字幕文件。

然而必须指出的是，日翻中的自动翻译准确度仍难以令人满意，再考虑到转录中可能产生的断句，误字等因素，自动翻译的结果只能作为有限的参考，请不要做过多期待。

## 我上传文件好慢
~上传和你的网速无关，这算是使用Colab的代价。等待上传的时间泡杯咖啡吧。~
除了本地上传的方式以外，现在已经可以直接从谷歌盘里选择要转换的文件。

## 为什么文件里出现了一句话一直重复？
这是Whisper的已知问题之一，和其转录原理有关，一些背景音较大或中间出现长时间没有人声的视频较容易出现此类问题，太长的视频建议分段转录以避免此类问题的出现几率。

此外，今后计划会允许用户直接调整一些模型参数以寻找最适合自己视频的设定。

关于这个问题可以参见 [这里](https://github.com/openai/whisper/discussions/192)和更多原repo的讨论部分。

## 为什么我处理第二个文件的时候就报错了
可能是进程仍然被占用导致资源不足，最简单的办法，重启应用从头运行即可。

## 我还有别的问题
欢迎随时发邮件到 admin@ikedateresa.cc. 一般24小时内都会回复。

