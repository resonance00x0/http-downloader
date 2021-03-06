# File joiner
If you split your files while downloading, all those parts need to be joined before you can use the downloaded file. For joining downloaded files, HTTP-Downloader offers you File joiner in [Android](#file-joiner-for-android) (Inbuilt), [Windows](#file-joiner-for-pc), [Linux](#file-joiner-for-pc) and [Mac](#file-joiner-for-pc)

### Additional options for File joiner
##### For illustration purpose take following case
> You had downloaded a `5GB` file as 3 parts with sizes `2.5GB`, `1.5GB` and `1GB`.

#### Append to first file
If this option is enabled, HTTP-Downloader writes contents of successive files to end of first file.
  - **When to use:**
    - your 1st file part is huge OR
    - you don't have enough storage left for full joined file (_in [above case](#for-illustration-purpose-take-following-case), if your remaining storage space is less than `5GB`, enable [Append to first file](#append-to-first-file)_) OR
    - If you have very few number (2 to 5) of huge sized file parts<br/>
    (in the [above case](#for-illustration-purpose-take-following-case), [Append to first file](#append-to-first-file) is highly recommended)
  - **Advantage:** This lets you join file parts with less extra storage space (_extra space required = `2.5GB` (sum of sizes of all file parts except 1st part) instead of `5GB` in [above case](#for-illustration-purpose-take-following-case)_) and with less time (_half the time in [above case](#for-illustration-purpose-take-following-case)_).
  - **Drawback:** If the joining process gets interrupted somehow, your 1st part will be permanently lost (_a programmer may still be able to recover it_) and you will need to re-download your 1st part

#### Delete after joining
If this is enabled, HTTP-Downloader will delete a file part as soon as it is joined to main (output) file.
  - **When to use:** Only when you don't have enough storage (`<5GB` in [above case](#for-illustration-purpose-take-following-case))
  - **Advantages:** Lets you join files with very less amount of extra space required (_extra space required = `2.5GB` (size of largest file part) instead of `5GB` in [above case](#for-illustration-purpose-take-following-case)_).
  - **Drawbacks:**
    - No change in overall time of joining
    - If joining gets interrupted in the midway, all the deleted files will be permanently lost (_Some data recovery tools may help to recover them_). You will need to re-download/recover all deleted files before you can retry file joining.


### Important notes
1. The order of the file parts need to be double checked. If you join them in wrong order, your download will definitely get corrupted.
2. You can combine [Append to first file](#append-to-first-file) and [Delete after joining](#delete-after-joining) to reduce overall time and extra storage required for joining. In [above case](#for-illustration-purpose-take-following-case), your joining will complete in **half the time** with only **`1.5GB` extra space** (_size of largest file part excluding 1st file_) if you enable both these options.

## File joiner for Android
File joiner is inbuilt in HTTP-Downloader for Android. Launch HTTP-Downloader, click on **+** icon on top right and choose File joiner. Follow on screen instructions to get all your files joined.

## File joiner for PC
[Download File Joiner from here.](https://resonance00x0.github.io/http-downloader/downloads/file_joiner.jar)<br>
File joiner is built on Java & it requires Java to be installed on your system to run. Follow [this tutorial](https://java.com/en/download/help/download_options.xml) to setup java on your system.<br>
Once Java is successfully installed, you can run the File Joiner like any other application by double clicking on the downloaded file.
If you can't run File Joiner, Open Command prompt (or Terminal on Mac & Linux) and type 
`java -jar`**_`<drag & drop file_joiner.jar here>`_**. (_Eg: `java -jar Downloads/file_joiner.jar`_) File joiner should start running normally. If you see some error, your java installation wasn't successful. Try re-installing Java

See also: 
- [About HTTP-Downloader](https://resonance00x0.github.io/http-downloader/)
- [What's new in HTTP-Downloader](https://resonance00x0.github.io/http-downloader/whats-new)
- [Common errors and FAQ](https://resonance00x0.github.io/http-downloader/faq)
- [Privacy policy](https://resonance00x0.github.io/http-downloader/privacy-policy)
- [Advanced mode](https://resonance00x0.github.io/http-downloader/advanced-mode)

[Suggest edits](https://github.com/resonance00x0/http-downloader/)
