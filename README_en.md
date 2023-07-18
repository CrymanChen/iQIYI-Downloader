# iQIYI-Downloader  
[[中文]](https://github.com/CrymanChen/iQIYI-Downloader/blob/main/README.md) | [English]  

### Project Name  
iQIYI-Downloader  

### Project Introduction  
A program written in Python, used for parsing iQIYI's m3u8 content, and downloading videos with the help of third-party tools. The current v1.1 version has optimized parsing logic and can achieve the following:  
· For TV dramas, free, VIP, and exclusive dramas can all be successfully parsed (which should be equivalent to all dramas…)  
· For movies, both free and VIP movies can be successfully parsed  
· ~~Cloud Cinema movies~~ (still being parsed, but the key can be obtained by other means)  

### Disclaimer  
This Python program is for learning purposes only and is a small work for my daily practice. Please do not use it for commercial purposes. Violators may violate relevant laws and accept corresponding penalties. This program uses [nilaoda's](https://github.com/nilaoda) [N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE) as the underlying download tool. Thanks to the author [nilaoda](https://github.com/nilaoda). In addition, consistent with all my other projects, I have no intention of infringing any individual or entity's rights. If such a situation happens, please contact me for timely next steps.  

### Instructions for Use  
0. Prerequisites  
To run this program, make sure you have the following environment:  
· Windows(R) device  
· Python 3  
· (Based on the previous one) Install third-party libraries via `pip install -r requirements.txt` (the same below *1. Run the program* Step 1)  
1. Run the program  
Currently, only tested on Windows. Please open a CMD window on your device and enter the following in the command line:  
Step 1: `pip install -r requirements.txt`  
Step 2: `python iqiyi.py`  
2. Enter "dash address"  
💡How to find the "dash address"?  
Please open the developer tools of the browser and search by keyword. For each video, there should be "only one" "dash address". The search result should be only one, and it should start with "cache.video.iqiyi.com".  
![20230717021050](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/61f4e570-da6c-4b91-b901-8ff75f98fd94)  
3. Enter the saved filename  
![image](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/476e1aca-e8e7-46e1-8fab-1ca396d1d27d)  
At the same time, you should be able to see the status code and delay (ms).  
In version v1.1, we have added colors to the status code and delay to try to improve the visual effect of the program.  
4. Invoke [N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE) to download  
![20230717021650](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/642ed2ee-c563-47ff-bdcb-bdc05cf434c2)  
5. You can choose whether to keep the parsed .m3u8 file  
![20230717022024](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/8c037e4f-73d0-42c3-90a3-417b66fc0a29)  

### Code Annotations and Explanations  
1. The value of `program = 're.exe'` should be consistent with the local path of [N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE). Use the absolute path if necessary.  
2. The value of `headers` is the default value. It can be modified according to the actual situation.  
[Appendix] cURL conversion address: https://curlconverter.com  
3. When entering the saved file name, the corresponding relationship between the input and the final result is:  
Output name ~~(default=output)~~: `Example Video`  
The final video name is `Example Video.mp4`  
The statement `~~(default=output)~~` has been deleted in version v1.1 because it was found that there was no default value set after testing.  
4. [Experimental Feature] [For Cloud Cinema Movies] This project is used to parse iQIYI's ordinary videos, but it can also be combined with my other project [WKS-KEYS](https://github.com/CrymanChen/WKS-KEYS), with [《iQIYI Cloud Cinema Encrypted Streaming Video Download Record》](https://mp.weixin.qq.com/s?__biz=Mzg2MzUyMDg5Mg==&mid=2247486660&idx=1&sn=9db713df121887183a4aff836a68a4b4&chksm=ce761dd7f90194c194a6c653cfb4a254aa8933f6379c06970324bc6d86d8c4477afa60279002#rd) as a reference, to get encrypted videos protected by Widevine.  
