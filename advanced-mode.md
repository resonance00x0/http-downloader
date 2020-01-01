# Advanced mode
### What is Advanced mode in HTTP-Downloader?
Advanced mode is a part of HTTP-Downloader app, which exposes app's raw potential to users with technical expertise.<br/>
To use Advanced mode tap on <b>+</b> icon at top right and click on <b>Advanced mode</b><br/>
Keep in mind that Advanced download is meant for geeks only. If you use it wrong, there is a high chance of your download getting failed or corrupted. No technical support will be given from our part in case you ran into trouble while using Advanced mode

### Why advanced mode?
Advanced mode gives you full control over all features of HTTP-Downloader. Unlike simple mode, all features are simultaneously available.
So advanced mode unlocks several features that were imposible/too_hard for simple mode to achieve
Sample problems: 
1. You need to download a 5GB file's part from 1GB to 3GB, but as 3 parts
2. You need to manually edit HTTP headers to get access to a file.


### Description for input fields in advanced mode
- Download link: The direct download URL of your file. If you go to this url from a browser, the download will start immediately (assuming supporting <a href="https://en.wikipedia.org/wiki/HTTP_cookie">cookies</a> are already set in that browser)
- File name: The visible name of your download file. File name should not contain these characters ```<>/?{}';"```
- Download folder: The folder to which the file will be written to. By default download folder is <b>/Internal storage/HTTP-Downloads</b>
- Offset: This is the byte position from which download starts. i.e. If you specify offset=2GB for a 5GB file, HTTP-Downloader will skip first 2GB and download remaining 3GB only
- Limit: This is the byte position at will download will stop. If you specify limit=3GB, for a 5GB file, download will start normally. But upon reaching 3GB, download terminates.
- NB: Offset & Limit can be used together to download specific region of the file. For example, for a 5GB file, if you set offset=2GB & limit=4GB, app will skip first 2GB, download next 2GB (reach 4GB mark) & terminate. The downloaded file will be of size 2GB (limit[4GB]-offset [2GB])
- Headers: <a>HTTP-Headers</a> which should be sent along with the request. Include cookies in header field as <a>Cookie field</a>. NB: Don't specify <a href=mozila>Content-Range</a> in Headers. It will be overridden by offset & limit fields. Use offset & limit fields to specify the content range.
- Split parts: You can make a file at most 99 parts (Minimum file size= TODO). & Download them parallel/one after other
- Parallel multi-part download
  - Some servers limit speed per connection. Using multi-part parallel download, you can bypass this issue by creating multiple connections together. Your download speed multiplies several times if parallel connections are made.
