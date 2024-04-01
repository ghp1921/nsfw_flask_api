# nsfw_flask_api:
基于flask实现的关于nsfw模型图像分类识别API接口

## Information:
这是一个基于flask开发的nsfw识别分类模型的api接口
上传部分仅包括纯代码部分。

## Usage
先执行app.py文件的main函数，启动flask服务

再执行use_api.py文件中的请求服务，返回local file内img.png图片的识别结果

## Identify result
```
eg:
result = {  
    'access_token': '647274',
    'id': '17119787910001',
    'result': {
        'cost_time': 3.3765790462493896s',
        'ends': {
            'nsfw_detector\\data\\test.png': {
                'drawings': 0.9776960611343384, 
                'hentai': 0.01737600564956665, 
                'neutral': 0.00417600991204381, 
                'porn': 0.0006983844214119017, 
                'sexy': 5.354164750315249e-05
            }
        }
    }
}
```
其中

drawings：安全工作环境下的动漫图片分类

hentai：非安全环境下的动漫图片分类

neutral：安全环境下的现实图片分类

porn：非安全环境下的色情图片分类

sexy：适当环境下的性感图片分类

结果分类应当以以上分类所占最大百分比为优。

## focus:
由于模型和虚拟环境太大，作者将其存放在百度网盘，需要自取

链接：https://pan.baidu.com/s/1B7whtrzf1QKo9JkI0OlQiQ 

提取码：nsfw

## download option:
### option1:
直接下载百度网盘中的压缩包，解压缩后你可以获得完整的项目包。

### option2:
若你不需要作者的虚拟化环境，在你拉取了github存储库的zip包之后，还需要下载网盘中的模型文件：nsfw.299x299.h5

## Directory:
-local file 文件夹    模拟客户端本地图片目录，内含用于上传到flask服务端识别的图片

-nsfw_detector 文件夹    模拟服务器端模型模块目录，内涵调用模型的文件'predict.py'，用于暂存接收到的图片资源的data文件夹，和模型文件nsfw.299x299.h5（github托管的压缩包没有，需要从网盘下载）。

-static 文件夹    无用

-templates 文件夹    无用

-venv 文件夹    虚拟化环境（github托管的压缩包没有，环境文件太大了，请按照requirements.txt内环境要求进行配置，若想直接使用，请下载网盘压缩包。）

-app.py py文件    用于启动flask服务

-requirements.txt txt文件    第三方库文档

-use_api py文件    用于模拟客户端发送请求

## Objectives:
仅供学习使用

模型出处：https://github.com/rockyzhengwu/nsfw

非常感谢！
