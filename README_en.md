# iQIYI-Downloader
[中文](https://github.com/CrymanChen/iQIYI-Downloader/blob/main/README.md) | [English]
⚠ The English version of README is done under the help of ChatGPT 4.0. You should be aware that some problems including grammar may occur unexpectedly even though it's the up-to-date newest and most powerful generative pre-trained transformer.

### Project Name
iQIYI-Downloader  

### Project Introduction
This is a program written in Python, designed to parse the m3u8 content of standard iQIYI videos and use third-party tools to download the videos.

### Disclaimer
This Python program is for learning purposes only, and is a small personal project for my daily practice. It is not intended for commercial use, and misuse may violate relevant laws and be subject to corresponding penalties.
The program uses [N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE) by [nilaoda](https://github.com/nilaoda) as the underlying download tool. I would like to express my gratitude to the author, [nilaoda](https://github.com/nilaoda). Also, consistent with all my other projects, I have no intention of infringing on any rights of any individual or entity. If any such infringement occurs, please contact me for immediate resolution.

### Instructions for Use
1. Run the program:  
   `pip install -r requirements.txt`  
   `python iqiyi.py`  
2. Enter the "dash address".  
   💡 How to find the "dash address"?  
   Please open the browser developer tool and search using the keyword. For each video, there should be "one and only one" dash address, and the search result should start with "cache.video.iqiyi.com".  
   ![20230717021050](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/61f4e570-da6c-4b91-b901-8ff75f98fd94)  
3. Enter the filename to save.  
   ![image](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/476e1aca-e8e7-46e1-8fab-1ca396d1d27d)  
   At this point, you should be able to see the status code and delay (ms).  
4. Invoke [N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE) for download.  
   ![20230717021650](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/642ed2ee-c563-47ff-bdcb-bdc05cf434c2)  
6. Decide whether to keep the parsed .m3u8 file.  
   ![20230717022024](https://github.com/CrymanChen/iQIYI-Downloader/assets/106590233/8c037e4f-73d0-42c3-90a3-417b66fc0a29)  

### Code Annotations and Instructions
1. The value of `program = 're.exe'` should be consistent with the local path of [N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE). Use an absolute path if necessary.
2. The value of `headers` is the default. It can be modified as needed.  
   [Attach] cURL conversion address: https://curlconverter.com
3. When entering the filename to save, the relationship between the input and the final result is as follows:  
   Output name (default=output): `Example Video`  
   The final video name is `Example Video.mp4`
4. [Experimental feature] This project is used to parse iQIYI standard videos, but it can also be used in conjunction with my other project [WKS-KEYS](https://github.com/CrymanChen/WKS-KEYS), with [iQIYI Cloud Cinema Encrypted Streaming Video Download Record](https://mp.weixin.qq.com/s?__biz=Mzg2MzUyMDg5Mg==&mid=2247486660&idx=1&sn=9db713df121887183a4aff836a68a4b4&chksm=ce761dd7f90194c194a6c653cfb4a254aa8933f6379c06970324bc6d86d8c4477afa60279002#rd) as a reference, to get Widevine-protected encrypted videos.
