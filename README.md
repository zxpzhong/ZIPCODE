# ZIPCODE
调用后该类后，会自动压缩目标目录所有代码。跑代码的时候，不是每次都记得会提交git更新，这个时候这个自动化压缩工具可以让你完美还原运行时的代码，推荐用法是：将目标压缩包写入日志文件夹，该文件夹同时也保存tensorboard的events文件，让每次运行的代码、日志、模型、events文件全部都在一个文件夹里面！！！
## 使用方法
```
from ZIPCODE import ZIPCODE
target_path = './'
target_name = 'test.zip'
source_path = './'
except_dir = []
except_file = []
ZIPCODE(target_path,target_name,source_path,except_dir,except_file)
```
 - target_path：存放压缩包目标目录，缺省为当前目录
 - target_name：目标压缩包名称，缺省为test.zip
 - source_path：源文件夹路径，缺省为当前目录
 - except_dir：需要除去的文件夹列表，缺省为空，推荐用法是除去文件夹中存放数据、模型大文件等的文件夹
 - except_file：需要除去的文件名，缺省为空
