# avsplusdecoder
An unoffcial AVS+(Advanced Video Standard Plus) Decoder

Notice:This is the decoder made by others.Please contact the author by Email(395579940@qq.com) or chat online with QQ(395579940) for any questions and technical support in both Chinese or English.This is not the open source yet,but free to use.

If you want to get more information for this standard,please get the view on the offcial website(www.avs.org.cn)
The offcial website contains many documents of this standard in Chinese & English.
For the specification of AVS+,you should pay to the offcial workgroup,and we will not provide it.

Without the permission of the developer of this decoder,I upload it just for more people to know this things.
I would not update immediately,please follow the developer's CSDN page for latest version.(http://download.csdn.net/user/chql1985)

AVS+ is a project for building Chinese Video & Audio's Encode & Decode standard in Broadcasting.
However,there are many hardware for encoding & decoding,but few software for personal usage.
In order to decoding AVS+ on PC and some other devices,here comes the decoder.

The decoder is made by an independent developer.
It's based on the standard documents "Adavanced coding of video and audio for broadcasting-Part I:video"(NO:GY/T 257.1-2012) released by SARFT(State Administration of Radio Film and Television).
Also the book "Advanced Video Coding Systems" published by Springer (ISBN:978-3-319-14242-5) provide the details of this standard.

The decoder now works in both Windows & Linux & Android.
You could run it in x86 or x64 mode with command.

The author says the decoder could decode 10Mbps 1080P with single core & thread in 50ms on I7 4770.
Here are some resource to show which the decoder works.

XAVSPlusPlayer.exe is a demo to play the private format SKG.In order to play SKG files,first you should extract the ES files from stream which include the AVS+ video stream.Then select"转换SKG" to convert ES file into SKG file.Finally,push"浏览..." and select the SKG file you have just generated.Now you could play the file.There is also a simple way,push "选择TS流文件" and select the TransportStream file which include the AVS+ video stream,and you will also see the video.But the simple way would not allow you drafting the time bar.

xavs_decoder.exe and xavs_decoder64.exe is the core of decoding in Windows enviroment.

e.g. xavs_decoder.exe example.es -mode -TopLeftCornerCoordinate1 -TopLeftCornerCoordinate2 -OutputLength -OutputWidth

e.g. xavs_decoder.exe example.es 0

e.g. xavs_decoder.exe example.es 1 0 0 960 540

The first parameter "mode",when mode=0,the decoder will just show the process of decoding to test performance;when mode=1,the decoder will show the image.You can also see the test_xavs_decodee_mode0.bat and test_xavs_decodee_mode1.bat as the example.

TestAVSDecoder32.x and TestAVSDecoder64.x is the core of decoding in Linux enviroment.

e.g.  ./TestAVSDecoder32.x example.es -mode -parameter1 -parameter2

e.g.  ./TestAVSDecoder32.x 1.es 0 0 0

e.g.  ./TestAVSDecoder32.x 1.es 1 400 300

The first parameter "mode",when mode=0,the decoder will export the yuv data as "test.yuv" in catelogue,the parameter1 is the start frame,the patameter2 is the end frame;when mode=1,the decoder will show the image,and the parameter1 is Output Length,the parameter2 is Output Width.Only the 32 support the SDL.

XAVSDecoderDemo_signed_aligned.apk is for Android enviroment.

There is also a special compile filters with LAVSplitter.It only decode the I frame and P frame for demo.
