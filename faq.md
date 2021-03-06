# HTTP Downloader FAQ
This section describes several frequently asked questions and its answers to easily troubleshoot your problem. If you still can't find a solution for your problem, you can always mail us at resonance00x0@gmail.com

### Can't locate files and folders in file picker?
In some devices, Primary storage spaces will be hidden by default. To unhide them follow these steps:
1. Tap on options (top right), and click on **Show SDCard** or **Show Internal** or anything similar (_varies with device_)<br>
![alt text](images/show_internal.png "Show internal menu in Android's file picker")<br>
2. Swipe from left and click on required storage medium<br>
![alt text](images/select_internal.png "Select required storage medium")<br>
3. Now choose your required folder/file

### How to find exact size of failed file in bytes
You will need to find the exact size of files (_in bytes_) to resume a download failed from another device. Also, if you use [Advanced mode](advanced-mode), you will need to find file size in bytes. See image below<br/>
![alt text](images/resume_failed_another_device.png "Start new task -> Resume failed download")
#### In Android (Note that these steps may vary based on apps used)
 - Download & install some geek friendly File Explorer apps
 - Locate your required file
 - Touch & hold and select Properties
 - Find text indicating file size as bytes; Make sure you don't select size on Disk<br/>
![alt text](images/prop_android.png "File size in bytes in Android")<br/>
**App used:** [Amaze File Manager](https://play.google.com/store/apps/details?id=com.amaze.filemanager)

#### In Mac OS
 - Browse to your required file using finder
 - Right click on the file & choose properties
 - Find text indicating file size as bytes; Make sure you don't select size on Disk<br/>
![alt text](images/mac_prop.png "File size in bytes in Mac")

#### In Windows
 - Browse to your required file using windows file explorer
 - Right click on the file & choose properties
 - Find text indicating file size as bytes; Make sure you don't select size on Disk<br/>
![alt text](images/prop_win.png "File size in bytes in Windows")

#### In linux
 - You already know how to find file size in bytes if you are using linux; Just make sure you don't select size on Disk


### What is continuous-reconnect mode?
Some websites provides high speed at the beginning of the download & later reduces it. This happens especially when you are trying to download a streaming video file. HTTP-Downloader can help you in such conditions by continuously reconnecting to server & restarting download from previously downloaded offset. In that case, the server is forced to provide high speed all the time. To maximize the download speed, you will need to configure auto-reconnection interval from settings (_**Download refresh interval**_). The optimum _**Download refresh interval**_ varies with server & your network speed.

But the increase in speed cannot be guaranteed. If the ping (_time required to initiate a connection_) is high, the download speed may become slow since the ping time compensates increase in speed.

**Enabling this option will always reduce speed for a normal download**. So this feature should be used only with streaming video type downloads.You can identify them by analyzing the download speed. The speed of such downloads will vary heavily. The speed may shoot up to 2MB/s for a second and then drop to 0KB/s-1KB/s for some time, and then again goes to 1MB/s-2MB/s and it repeats.

**Enabling this may not guarantee increase in download speed. This may vary based on several factors as discussed above.**

### How to start download from another browser?
HTTP-Downloader relies on Android's native WebView for displaying webpages. Since it is not as advanced as modern browsers, the pages may look choppy and some times download may not start. But HTTP-Downloader is heavily extensible. You can start download from third party browsers too (even though it requires some technical expertise). Follow these steps to grab a download from other browsers like Chrome:
1. Install and configure any network monitoring tool (For example: https://play.google.com/store/apps/details?id=app.greyshirts.sslcapture).
2. With the network monitor running, go to the website from any browser and start download. Cancel download when it reaches around 200 KB.
3. Go back to network monitor and identify the network request corresponding to the file you are downloading.
4. Copy the `URL` and `request headers` for the download.
5. Now open HTTP-Downloader and navigate to Advanced download mode.
6. Paste the copied `URL` to the **Download link** field and paste `request headers` to **Headers** field.
7. Uncheck **Create a blank file first** option (to avoid problems when your download gets failed).
8.    
_**If you want to start a fresh download:**_
- Select an output folder/file and click on proceed button (bottom right) to start download

_**If you want to resume a failed download:**_
- Click on **Choose file** and select to your failed file.
- Click on proceed button (bottom right) to start download

**Note:** _If you are doing this to resume an interrupted download from HTTP-Downloader, this will create a new download instance. But don't worry. The file will be resumed from where it stopped (if the server supports it). The previous download task can be safely deleted (without file)._


### Where should I report bugs or give feedbacks?
Please use **_Report a bug / Suggest a new feature_** option in app **_settings_** for reporting bugs, feedbacks and queries. We will be assisting you within a day (average time of reply: 2 hours) after you successfully report the bug.<br>
When reporting bugs, please attach full details of the issue including your download link, download location (Internal storage/SD-card), Device model, Method of downloading, app logs, screenshots or screen record videos and every possible detail you could share. This makes debugging easier & ensures your issue to be triaged fast.<br>
**We will be offering In-app rewards for critical/high-priority bug reports once triaged** (Note that the decision of approving in-app rewards is solely ours)


### Is there a desktop alternative for HTTP-Downloader?
As of now, we don't have a desktop alternative for HTTP-Downloader. But due to heavy support from our Android users, we have decided to build an HTTP-Downloader for Windows desktop. We are planning to make it available in Windows store from next year (mid 2021) onwards. We have devoted a special windows development team for this purpose. Your continuous help and support is heavily influencing our productivity & development speed.

### Is there an iOS alternative for HTTP-Downloader?
No we don't have an iOS alternative. We don't plan to make one either. Sorry for the inconvenience.

Contact us: resonance00x0@gmail.com

See also: 
- [About HTTP-Downloader](https://resonance00x0.github.io/http-downloader/)
- [What's new in HTTP-Downloader](https://resonance00x0.github.io/http-downloader/whats-new)
- [Advanced mode](https://resonance00x0.github.io/http-downloader/advanced-mode)
- [Privacy policy](https://resonance00x0.github.io/http-downloader/privacy-policy)
- [File joiner](https://resonance00x0.github.io/http-downloader/file-joiner)

[Suggest edits](https://github.com/resonance00x0/http-downloader/)
