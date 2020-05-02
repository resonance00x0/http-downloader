# HTTP-Downloader

HTTP-Downloader is the most advanced downloading tool ever built. Unlike traditional download managers, HTTP-Downloader offers you much more features.<br>
[Click here to install HTTP-Downloader](#downloads)
> Note: HTTP-Downloader is currently in beta mode. Please help us by reporting bugs, if you find any, through App's settings -> Report bugs. [Read more..](https://resonance00x0.github.io/http-downloader/report-bugs)

## HTTP-Downloader Key features
### Resume failed downloads
HTTP-Downloader can request the remaining part of any file from servers. With this, you can resume failed downloads from even third party apps like Google Chrome, FireFox etc.. The failed file can be resumed from where it stopped without wasting even extra 10KB. _Note: We don't guarantee 100% compatibility with any third party app even though it works fine in most cases._
##### How to use
1. Launch app. Tap on **+** icon on top right. Select **Start new task**
2. Now select **Resume a failed download** & follow on screen instructions

### Download using multiple devices together
As HTTP-Downloader can request download from any byte position, it can split your download among your devices. So, if you have 3 Android devices and a 6GB file to download, each device will download subsequent 2GB part. Since devices can download files in parallel, effectively, you can achieve 3X speed for download. After completion of downloads, you can join them from any device (Android, Windows, Linux or Mac) to get full file
##### How to use
1. Launch app. Tap on **+** icon on top right. Select **Start new task**
2. Now select **Download using 2 (_or more_) devices** & follow on screen instructions

### Forget about storage left on device
Even if you are low on storage, you can download huge file as small parts. Download a part of your file, which fits your device's storage, move it to a storage medium, download next part and continue. After completing, you can join all the parts to get your full file.
##### How to use
1. Launch app. Tap on **+** icon on top right. Select **Start new task**
2. Now select **Download a File part** & follow on screen instructions

### Overcome size limits
Most of the external SD-Cards can't handle files of size more than 4GB. So you cannot download a file of size 5GB to an SDCard with even 50GB free. In such cases HTTP-Downloader comes handy as it can automatically split files to several parts while downloading. So you can download the 5GB file as two 2.5GB parts, and later join them from a PC. _This problem exists for some old device's internal storage also_
##### How to use
1. Launch app. Tap on **+** icon on top right. Select **Start new task**
2. Now select **Download as several parts** & follow on screen instructions

### Bypass speed restrictions
Some web-servers limit speed per connection to limit their network traffic. In such cases, you can simply download file as two or more different parts. Since it makes several parallel connections, your speed hikes multiple times. For servers enforcing speed limit per IP, try [Download using multiple devices together](#download-using-multiple-devices-together)
##### How to use
1. Launch app. Tap on **+** icon on top right. Select **Start new task**
2. Now select **Download as several parts** & follow on screen instructions

### Continuous re-connection
Some web-servers provide high speeds at beginning of download and later reduces it heavily. This happens especially with video streaming servers. HTTP-Downloader can continuously re-connect to the server and ask for fresh download periodically. This assures high speed all the time as the connection is renewed frequently (read more [here](https://resonance00x0.github.io/http-downloader/faq#what-is-continuous-reconnect-mode))

### Download directly to cloud storage
Since HTTP-Downloader uses modern [Storage Access Framework](https://developer.android.com/guide/topics/providers/document-provider) of Android, users can choose any writable location from document picker UI including their cloud drives. So download will be directly tunnelled to their cloud storage without using any storage space on your device's local storage.<br/>
_Since this feature is an addon and we don't natively support it, it is available only from advanced mode_. Native support for Google drive is in our todo list and will be ready within a couple of months after release.
##### How to use
1. Launch app. Tap on **+** icon on top right. Select **Advanced download**.
2. Click on browser icon to go to browser and click on your download link.
3. Choose **Choose file** option. From file picker, choose a file in your cloud drive.
4. Uncheck **Create a blank file first** to avoid double network usage (firstly for making file & then for downloading).
5. Click on next icon to review & click again to start download.

To improve the app, we need your valuable suggestions and bug-reports. Please let us know if you faced any problem while using our app. [Click here to read more](https://resonance00x0.github.io/http-downloader/report-bugs)

Contact us at: resonance00x0@gmail.com

#### Downloads
[Click here to download the app from Google play store](https://play.google.com/store/apps/details?id=resonance.http.httpdownloader)

![alt text](https://resonance00x0.github.io/http-downloader/images/play_store_link_qr.png "Google Play store link")

## Credits
We thank the following sources for providing us free assets to develop HTTP-Downloader
1. [zxing](https://github.com/zxing/zxing) for QR code scanner engine
2. QR code icon used in built-in browser is made by [Pixel perfect](https://www.flaticon.com/authors/pixel-perfect) from www.flaticon.com

See also: 
- [What's new in HTTP-Downloader](https://resonance00x0.github.io/http-downloader/whats-new)
- [Common errors and FAQ](https://resonance00x0.github.io/http-downloader/faq)
- [Details of Advanced mode](https://resonance00x0.github.io/http-downloader/advanced-mode)
- [Privacy policy](https://resonance00x0.github.io/http-downloader/privacy-policy)
- [File joiner](https://resonance00x0.github.io/http-downloader/file-joiner)

[Suggest edits](https://github.com/resonance00x0/http-downloader/)
