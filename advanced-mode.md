# Advanced mode
### What is Advanced mode in HTTP-Downloader?
Advanced mode is a part of HTTP-Downloader app, which exposes app's raw potential to users with technical expertise.<br/>
To use Advanced mode tap on <b>+</b> icon at top right and click on <b>Advanced mode</b><br/>
_Keep in mind that Advanced download is meant for geeks only. If you use it wrong, there is a high chance of your download getting failed or corrupted. No technical support will be given from our part in case you ran into trouble while using Advanced mode_

### Why advanced mode?
Advanced mode gives you full control over all features of HTTP-Downloader. Unlike simple mode, all features are simultaneously available.
So advanced mode unlocks several features that were imposible/too_hard for simple mode to achieve
##### Sample problems: 
1. You need to download a 5GB file's part from 1GB to 3GB, but as 3 parts
2. You need to manually edit HTTP headers to get access to a file.


### Description for input fields in advanced mode
#### Download link
The direct download URL of your file. If you go to this url from a browser, the download will start immediately without landing on an intermediate page (assuming supporting [cookies](https://en.wikipedia.org/wiki/HTTP_cookie) are already set in that browser)

#### File name
The visible name of your download file. File name should not contain these characters `<>/?{}';"`. This option is available only if [Choose folder](#choose-folder) is selected

#### Choose folder
The folder to which the download will be written to. By default, the download folder is **Internal storage/HTTP-Downloads**. 

#### Choose file
This option lets you select output file directly. Since Android's [Storage access framework](https://developer.android.com/guide/topics/providers/document-provider) supports more locations including cloud drives with when choosing file instead of folder, you can download files directly to cloud drives like Google drive (You should have corresponding cloud's app installed & you should be signed into it before you can choose your output file). When you choose this option, some [File name](#file-name) and [Split to parts](#split-to-parts) will be disabled. **Note: If you are intending to download to cloud storage, we recomment turning off [Create a blank file first](#create-a-blank-file-first) to avoid double data usage**.

#### Offset
This is the byte position from which download begins. If you specify `offset = 2GB`, HTTP-Downloader will skip first `2GB` and starts download from `byte position = 2147483648`. If you have selected an already existing, non-zero sized output file, the file size will be added to the offset. **For example:** _Assume you have a `5GB` file to download, but your friend offered to help you by downloading first `2GB` part. Now you need to download last `3GB` only. You started the download by specifying `offset = 2GB`. But your download got interrupted when it reached `1GB`. Now you need to download remaining part of the file to the top of the already downloaded `1GB` file._ This time you need need not change your offset to `3GB`. Continue with `offset = 2GB` & HTTP-Downloader will automatically add file size with your offset when it starts download. **Default value = 0 byte**

#### Limit
This is the byte position at will download will terminate. If you specify `limit = 3GB` download stops when it reaches `byte position = 3221225472`. In the example described in [Offset](#offset) section, your friend need to set `limit = 2GB` when he starts download. **Default value = total size of your download**

> **Note 1:** Offset & Limit can be used together to download specific region of the file. For example, for a `5GB` file, if you set `offset = 2GB` & `limit = 4GB`, app will skip first `2GB`, download next `2GB` (reach `4GB` mark) & terminate. The downloaded file will be of size `2GB` (`limit -offset` = `4GB - 2GB`)

> **Note 2:** While dealing in byte positions offset is inclusive and limit is exclusive. For example if set `offset = 4 bytes` and `limit = 8 bytes` the downloaded file will contain bytes in following positions of the download `[4, 5, 6, 7]; length=4`

#### Headers
[HTTP-Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers) which should be sent along with the request. [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cookie) do no have a separate field. Include them in HTTP-Headers. **Note:** Don't specify [Content-Range](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Range) in Headers. It will always be overridden by [offset](#offset) & [limit](#limit) fields. Use [offset](#offset) & [limit](#limit) fields to specify the content range.

#### Split to parts
Use this option to get your download automatically split to several parts.
- **Split to:** How many parts do you want this file to be made into. You can make a file at most 99 parts
- **Download in parallel:** All the file parts will be downloaded in parallel. Use this when your download host is limiting speed per connection.
- **Download one after the other:** The next download will start immediately after finishing its preceding one. Use this method when you are downloading a `4GB+` file to vFat/FAT32 formatted internal storage or external SD-Card.

#### Create a blank file first
Checking this option will create a blank file of size equivalent to your download to the specified output location before starting download. It is recommended as it reserves space for download so that it won't get failed in between due to lack of storage. But this option requires writing to your storage twice; one for creating empty file and another for writing the contents.<br/>
**Avoid using this option when**
- You have huge amount of storage space left in comparison with your download & you are sure that it won't be exhaused during download. In such case you are wasting time writing blank file.
- You are downloading to cloud drives. This may use data twice (`3/2` times, to be precise) as what is actually required
- You are intending to clear HTTP-Downloader's app data without backing up while download is in progress or is paused. It may cause HTTP-Downloader to loose how much data has already been written and it will restart download from beginning.
- Your download may get interrupted too many times. In that case HTTP-Downloader will use slightly more data than actually required.

See also: 
- [About HTTP-Downloader](https://resonance00x0.github.io/http-downloader/)
- [What's new in HTTP-Downloader](https://resonance00x0.github.io/http-downloader/whats-new)
- [Common errors and FAQ](https://resonance00x0.github.io/http-downloader/common-errors)
- [Privacy policy](https://resonance00x0.github.io/http-downloader/privacy-policy)
- [File joiner](https://resonance00x0.github.io/http-downloader/file-joiner)

[Suggest edits](https://github.com/resonance00x0/http-downloader/)
