#HackingWindowsTaskManager

### Line
<img src="https://github.com/mincongzhang/HackIntoWindowsTaskManager/raw/master/cpu_50.bmp" alt="1" title="1" height="400"/>


### Sin Wave
<img src="https://github.com/mincongzhang/HackIntoWindowsTaskManager/raw/master/cpu_sin.bmp" alt="1" title="1" height="400"/>


### Reference:  
Draw Sin Wave  
http://book.douban.com/annotation/13530271/  
http://noalgo.info/444.html (multithreading)  
http://blog.renren.com/share/185447585/6940521336  

Play Animation:  
http://www.bilibili.com/video/av620375/  
http://www.bilibili.com/video/av2281028/  
http://me.ivydom.com/archives/cppbadapple.html  
http://timothyqiu.com/archives/bad-apple-in-windows-task-manager/  
http://translate.google.co.uk/translate?hl=en&sl=zh-CN&u=http://timothyqiu.com/archives/bad-apple-in-windows-task-manager/&prev=search  

Draw in Windows  
Learning to Draw Basic Graphics in C++  
http://www.informit.com/articles/article.aspx?p=328647&seqNum=3  
Transparent Bitmaps  
http://www.winprog.org/tutorial/transparency.html  
Bitmaps, Device Contexts and BitBlt  
http://www.modula2.org/win32tutor/bitmaps.php  
Timer  
http://www.modula2.org/win32tutor/animation.php  
Capture a window and save it  
http://www.codeproject.com/Articles/19192/How-to-capture-a-Window-as-an-Image-and-save-it  
http://stackoverflow.com/questions/7292757/how-to-get-screenshot-of-a-window-as-bitmap-object-in-c
Edit Pixel  
http://stackoverflow.com/questions/2750988/c-reading-and-editing-pixels-of-a-bitmap-image  

DavesFrameClass(that cpu window)  
http://blogs.msdn.com/b/oldnewthing/archive/2007/07/25/4036123.aspx

TODO: read from cfg file



Make pixels transparent  
https://social.msdn.microsoft.com/Forums/en-US/88c7d2fc-32fe-44ce-b367-48d4fd114c09/how-to-replace-two-colors-in-hbitmap-in-wince-?forum=vssmartdevicesnative
1. Use CreateBitmap() or CreateComatibleBitmap() to create a new HBITMAP with the same size as the original.

2. Use FillRect() to fill the entire new HBITMAP with the new color. 

3. Use TransparentBlt() to copy the image from the old HBITMAP to the new HBITMAP. Use the color you want to replace as the transparent color.

Now your old image will appear in the new bitmap; the old color will be invisible and the color underneath will be seen. Now you have changed the color of the bitmap.
