# iQIYI-Downloader

### 项目名称
iQIYI-Downloader  

### 项目介绍
一个用Python编写而成，用于解析爱奇艺普通视频的m3u8内容，并借助三方工具下载视频的程序。  

### 免责声明
本Python程序仅用于学习用途，为本人日常练手的一个小作品。请勿将其用于商业用途，违者可能违反相关法律，并接受对应处罚。  
本程序使用到了[nilaoda](https://github.com/nilaoda)的[N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE)作为底层下载工具，在此向作者[nilaoda](https://github.com/nilaoda)表示感谢。此外，与本人其他所有项目一致，本人无意侵犯任何个人或实体的任何权利，若该情况不甚发生，烦请联系本人以便及时进行下一步处理。  

### 使用说明
1. 运行程序
`pip install -r requirements.txt`
`python iqiyi.py`  
2. 输入“dash地址”  
💡如何查找“dash地址”？  
请打开浏览器开发者工具，通过关键字进行查找。对于每个视频，“dash地址”应“有且只有一个”，查找结果应只有一个，且应以“cache.video.iqiyi.com”开头。  
![20230717021050](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/61f4e570-da6c-4b91-b901-8ff75f98fd94)  
3. 输入保存文件名  
![image](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/476e1aca-e8e7-46e1-8fab-1ca396d1d27d)  
与此同时，你应该已经能看到状态码和延时（ms）。  
4. 调用[N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE)进行下载  
![20230717021650](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/642ed2ee-c563-47ff-bdcb-bdc05cf434c2)  
6. 可决定是否保留解析生成的.m3u8文件  
![20230717022024](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/8c037e4f-73d0-42c3-90a3-417b66fc0a29)  

### 代码注释和说明
1. '''program = 're.exe'
'''的值请与[N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE)的本地路径一致。必要时请使用绝对路径。
2. `headers`的值为默认值。可根据实际情况进行修改。  
[附]cURL转换地址：https://curlconverter.com
3. 输入保存文件名时，输入和最终结果的对应关系为：
Output name (default=output): `示例视频`  
最终的视频名称为`示例视频.mp4`
4. [实验性功能]本项目用于解析爱奇艺普通视频，但也可配合我的另一个项目[WKS-KEYS](https://github.com/CrymanChen/WKS-KEYS)，以[《爱奇艺云影院加密流媒体视频下载纪实》](https://mp.weixin.qq.com/s?__biz=Mzg2MzUyMDg5Mg==&mid=2247486660&idx=1&sn=9db713df121887183a4aff836a68a4b4&chksm=ce761dd7f90194c194a6c653cfb4a254aa8933f6379c06970324bc6d86d8c4477afa60279002#rd)作为参考，获取受Widevine保护的加密视频。
