# nsfw_flask_api:
基于flask实现的关于nsfw模型图像分类识别API接口

# information:
这是一个基于flask开发的nsfw识别分类模型的api接口
上传部分仅包括纯代码部分。

## focus:
由于模型和虚拟环境太大，作者将其存放在百度网盘，需要自取

链接：https://pan.baidu.com/s/1B7whtrzf1QKo9JkI0OlQiQ 

提取码：nsfw

## download option:
### option1:
直接下载百度网盘中的压缩包，解压缩后你可以获得完整的项目包。

### option2:
若你不需要作者的虚拟化环境，在你拉取了github存储库的zip包之后，还需要下载网盘中的模型文件：nsfw.299x299.h5

## Project directory structure:
-local file 文件夹    模拟客户端本地图片目录，内含用于上传到flask服务端识别的图片

-nsfw_detector 文件夹    模拟服务器端模型模块目录，内涵调用模型的文件'predict.py'，用于暂存接收到的图片资源的data文件夹，和模型文件nsfw.299x299.h5（github托管的压缩包没有，需要从网盘下载）。

-static 文件夹    无用

-templates 文件夹    无用

-venv 文件夹    虚拟化环境（github托管的压缩包没有，环境文件太大了，请按照requirements.txt内环境要求进行配置，若想直接使用，请下载网盘压缩包。）

-app.py py文件    用于启动flask服务

-requirements.txt txt文件    第三方库文档

-use_apirequests.py py文件    用于模拟客户端发送请求

## Objectives:
仅供学习使用
