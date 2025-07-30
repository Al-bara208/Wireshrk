تحليل ملف pcap مشبوه بستخدام Wireshrk  

بدأت بتحليل الملف بستخدام Wireshrk وبستخدام فلتر  (http.request or tls.handshake.type eq 1) and !(ssdp) استطعت التوصل الى الاتي :

لاحظت اثناء بحثي في البكجات شكل غريب لعنوان URL فقمت بالضغط عليه والبحث في تفاصيله واكتشفت اسم الدومين الخاص به وايضا اكتشفت انه غريب فقمت بالتحري عنه بستخدام virustotal وفعلا تم تصنيفه ك Malware 
بعد ذالك اردت ان اعرف عنوان ip source الجهاز المصاب فوجدته في عامود source  والماك الخاص به في التفاصيل ايضا 
بعد ذالك استطعت الاجابة عن الاسئلة التالية : 

ما هو عنوان IP الخاص بعميل Windows المصاب؟

الاجابة : 10.6.13.133 

ما هو عنوان MAC الخاص بعميل Windows المصاب؟

الاجابة : ac:97:df (24:77:03:ac:97:df)

ما هو اسم المضيف لعميل Windows المصاب؟

الاجابة : 

في البكج GET : 

 event-time-microsoft.org 

في البكج post : 

eventdata-microsoft.live








Analyzing a Suspicious .pcap File Using Wireshrk

I began analyzing the file using Wireshrk and using the filter (http.request or tls.handshake.type eq 1) and !(ssdp). I was able to find the following:

While searching through the packages, I noticed a strange URL. I clicked on it and looked into its details. I discovered its domain name, which was also strange. I investigated it using virustotal, and it was indeed classified as malware.

After that, I wanted to know the IP address of the infected device. I found it in the Source column, and its MAC address was also listed in the Details column.

After that, I was able to answer the following questions:

What is the IP address of the infected Windows client?

Answer: 10.6.13.133

What is the MAC address of the infected Windows client?

Answer: ac:97:df (24:77:03:ac:97:df)

What is the hostname of the infected Windows client?

Answer:

In the GET package:

event-time-microsoft.org

In the POST package:

eventdata-microsoft.live
