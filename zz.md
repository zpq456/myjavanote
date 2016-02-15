#ÀÚ¹ÙÀÇ Æ¯Â¡
ÀÚ¹Ù´Â ÀÚ¹Ù °¡»ó ¸Ó½ÅÀ» ½á¼­ ÇÁ·Î±×·¥À» µ¹¸°´Ù.
**JVM(ÀÚ¹Ù°¡»ó¸Ó½Å)**Àº ÀÚ¹Ù ¹ÙÀÌÆ®ÄÚµå¸¦ ½ÇÇàÇÒ ¼ö ÀÖ´Â ÁÖÃ¼ÀÌ´Ù.
ÀÚ¹Ù ¹ÙÀÌÆ®ÄÚµå´Â ÇÃ·§Æû¿¡ µ¶¸³ÀûÀÌ¸ç ¸ðµç ÀÚ¹Ù °¡»ó ¸Ó½ÅÀº
ÀÚ¹Ù °¡»ó ¸Ó½Å ±Ô°Ý¿¡ Á¤ÀÇµÈ ´ë·Î ÀÚ¹Ù ¹ÙÀÌÆ®ÄÚµå¸¦ ½ÇÇàÇÑ´Ù.
µû¶ó¼­ **C¿Í´Â ´Ù¸£°Ô ¸ðµç ÄÄÇ»ÅÍ¿¡¼­ ½ÇÇàÀÌ °¡´ÉÇÏ´Ù.**

Java ÄÄÆÄÀÏÀ» ÇÏ¸é classÆÄÀÏÀ» »ý¼ºÇÏ°Ô µÇ°í JVMÀÌ ½ÇÇàÀ»
ÇÏ°Ô µÈ´Ù. C¿Í´Â ´Ù¸£°Ô ¸µÅ©µ¿ÀÛÀÌ ¾ø´Ù.

JDK´Â ÀÚ¹Ù ÀÀ¿ë °³¹ß È¯°æÀ¸·Î °³¹ßÀ» ÇÏ±â À§ÇØ¼­ ÇÊ¿äÇÏ°í
JRE´Â ÀÚ¹Ù ½ÇÇà È¯°æÀ¸·Î ½ÇÇàÀ» ÇÏ±â À§ÇØ¼­ ÇÊ¿äÇÏ´Ù.
(JRE¿¡´Â JVMµµ Æ÷ÇÔµÇ¾î ÀÖ´Ù.)

ÀÚ¹Ù´Â ¸ÖÆ¼½º·¹µå¸¦ ¿î¿µÃ¼Á¦ÀÇ µµ¿ò ¾øÀÌ ÀÚÃ¼ÀûÀ¸·Î Áö¿øÇØÁØ´Ù.
¸ÖÆ¼½º·¹µå´Â ÇÁ·Î±×·¥´ç 1°³¾¿¸¸ ÇÒ´çµÇ´Â ÇÁ·Î¼¼½º¿Í´Â ´Ù¸£°Ô
´Ù¼öÀÇ ½º·¹µå°¡ ÇÏ³ªÀÇ ÇÁ·Î±×·¥ ¾È¿¡¼­ º´·ÄÃ³¸®¸¦ ÇØÁØ´Ù.

##ÀÚ¹ÙÀÇ »ç¿ë
ÀÚ¹ÙÀÇ ±âº»Å¸ÀÔ
-boolean(1byte, true or false)
-char(2byte, Unicode)
-byte(1byte)
-short(2byte)
-int(4byte)
-long(8byte)
-float(4byte)
-double(8byte)

·¹ÆÛ·±½º Å¸ÀÔ
-Å¬·¡½º¿¡ ´ëÇÑ ·¹ÆÛ·±½º
-ÀÎÅÍÆäÀÌ½º¿¡ ´ëÇÑ ·¹ÆÛ·±½º
-¹è¿­¿¡ ´ëÇÑ ·¹ÆÛ·±½º

»ó¼öÀÇ »ç¿ë
final¸¦ ºÙ¿©¼­ »ç¿ëÇÏ¸ç ÃÊ±â°ªÀ» ÁöÁ¤ÇÏ°í ½ÇÇàÁß °ªÀÌ
º¯°æµÇÁö ¾Ê´Â´Ù.

System.in
Å°º¸µå¿Í ¿¬°áµÈ ÀÚ¹ÙÀÇ Ç¥ÁØ ÀÔ·Â ½ºÆ®¸² À¸·Î ÀÔ·ÂµÇ´Â Å°¸¦
¹ÙÀÌÆ®·Î ¸®ÅÏÇÏ´Â Àú¼öÁØÀÇ ½ºÆ®¸²ÀÌ´Ù. ÀÌ¸¦ »ç¿ëÇÏ¸é ¹ÙÀÌÆ®¸¦ 
¹®ÀÚ³ª ¼ýÀÚ·Î º¯È¯ÇÏ´Â ¸¹Àº ¾î·Á¿òÀÌ ÀÖ´Ù.

class
Å¬·¡½º´Â ¸Þ¸ð¸®¿¡ ÇÒ´çµÇÁö ¾Ê°í ÇüÅÂ¸¸ ÀÖ´Â°ÍÀÌ¸ç ÀÌ¸¦ 
»ç¿ëÇÏ·Á¸é °´Ã¼¸¦ »ý¼ºÇÏ¿© ½á¾ß ÇÑ´Ù. ºñ±³ÇÏÀÚ¸é Å¬·¡½º´Â
¼³¸í¼­ °´Ã¼´Â Á¦Ç°ÀÌ¶ó°í ÇÒ ¼ö ÀÖ´Ù.

new
°´Ã¼¸¦ »ý¼ºÇÒ¶§´Â new¸¦ »ç¿ëÇÏ¿© »ý¼ºÇÑ´Ù
(ex. a(º¯¼ö¸í) = new b(Å¬·¡½º¸í))

ÀÚ¹ÙÀÇ ¿¹¿ÜÃ³¸®
¿À·ù(Error)´Â ½Ã½ºÅÛÀûÀÎ ºñ»óÈ²ÀÌ´Ù. ¿¹¿Ü(Exception)´Â °³¹ßÀÚ°¡
±¸ÇöÇÑ ·ÎÁ÷¿¡¼­ ¹ß»ýµÈ´Ù. µû¶ó¼­ °³¹ßÀÚ°¡ ¿¹¿ÜÃ³¸®¸¦ ÇØ¼­
Ã³¸®¹æ¹ýÀ» ¸íÈ®È÷ ¾Ë°í Àû¿ëÇØ¾ß ÇÑ´Ù. 
ÀÚ¹Ù´Â ¿¹¿Ü(Exception)°¡ »ý°åÀ» ¶§ ÇØ´ç ¿¹¿Ü¸¦ ÀÚ½ÅÀÌ ÇØ°áÇÏ°Å³ª ÀÚ½Åº¸´Ù
»óÀ§ÀÇ Å¬·¡½º¿¡ ÀÌ¸¦ ³Ñ°Ü ÇØ°á½ÃÅ°°Ô ÇÑ´Ù.
1. try~catch~finally
try±¸¿ª¿¡¼­ ¹®Á¦°¡ ¾øÀ¸¸é ³Ñ¾î°¡°í ¿À·ù°¡ ³ª¸é ÇØ´ç 
¿À·ùÀÏ¶§ÀÇ catch±¸¿ªÀ» ÁøÇà½ÃÅ²´Ù. ÀÌ¸¦ ÅëÇØ¼­ ¿À·ù°¡
³ª¸é ±× Å¬·¡½º ¾È¿¡¼­ ÇØ°áÀ» ÇÒ ¼ö ÀÖ´Ù.
finally´Â try¸¦ °ÅÄ¡µç catch¸¦ °ÅÄ¡µç »ó°üÇÏÁö ¾Ê°í
¹«Á¶°Ç ÁøÇàµÈ´Ù. µû¶ó¼­ ¿À·ùÀÇ À¯¹«¿¡ °ü°è¾øÀÌ ²À ÇØ¾ß
ÇÏ´Â ÀÛ¾÷À» ³Ö¾î¾ß ÇÒ ¶§ »ç¿ëµÈ´Ù.
2. throwable Å¬·¡½º
ÀÚ½Åº¸´Ù ÇÑ´Ü°è »óÀ§ÀÇ Å¬·¡½º¿¡ ¿¹¿ÜÃ³¸®¸¦ ³Ñ°ÜÁØ´Ù.
ÀÌ¶§ throwable Å¬·¡½º´Â ¿¹¿ÜÃ³¸®¸¦ ÇÒ ¼ö ÀÖ´Â ÃÖ»óÀ§ Å¬·¡½ºÀÌ´Ù.

°¡ºñÁö ÄÃ·º¼Ç
°¡ºñÁö ÄÃ·¢¼ÇÀº °¡ºñÁö ÄÃ·ºÅÍ°¡ ¸Þ¸ð¸®ÀÇ Èü ¿µ¿ª¿¡ ÇÒ´çµÈ
´õ ÀÌ»ó »ç¿ëµÇÁö ¾Ê´Â °´Ã¼¸¦ ´Ù¸¥ °´Ã¼°¡ »ç¿ëÇÒ ¼ö ÀÖµµ·Ï
Á¦°ÅÇÏ´Â °ÍÀ» ¸»ÇÑ´Ù.µû¶ó¼­ ÀÚ¹Ù´Â ¸Þ¸ð¸® °ü¸®¸¦ °³¹ßÀÚ°¡ 
Á÷Á¢ ÇØ¾ß Çß´ø C¿Í´Â ´Ù¸£°Ô ÀÚµ¿À¸·Î ¸Þ¸ð¸® °ü¸®¸¦ ÇØ ÁØ´Ù.

Á¦³×¸¯
Å¬·¡½º ³»ºÎ¿¡¼­ »ç¿ëÇÒ µ¥ÀÌÅÍ Å¸ÀÔÀ» ¿ÜºÎ¿¡¼­ ÁöÁ¤ÇÏ´Â ±â¹ýÀÌ´Ù.
<>»çÀÌ¿¡ ¾î¶² µ¥ÀÌÅÍ Å¸ÀÔÀ» »ç¿ëÇß´À³Ä¿¡ µû¶ó ´Þ¶óÁö´Âµ¥
µ¥ÀÌÅÍ Å¸ÀÔÀ» È®Á¤ÇÏÁö ¾Ê°í ÀÎ½ºÅÏ½º¸¦ »ý¼ºÇÒ ¶§ µ¥ÀÌÅÍ Å¸ÀÔÀ»
ÁöÁ¤ÇÏ´Â°ÍÀÌ °¡´ÉÇÏ´Ù.Á¦³×¸¯À» ¾²°ÔµÇ¸é ÄÚµåÁßº¹À» ¸·°í 
Å¸ÀÔ ¾ÈÁ¤¼ºÀ» ³ôÀÏ ¼ö ÀÖ´Ù.

int¿Í Integer
ÀÚ¹Ù¿¡¼­ Á¤¼ö¸¦ Ç¥ÇöÇÏ´Â ÀÚ·áÇüÀ¸·Î int¿Í Integer¸¦ »ç¿ëÇÑ´Ù.
int´Â Á¤¼ö¸¦ Ç¥ÇöÇÏ´Â ÀÚ·áÇüÀ¸·Î ¿ì¸®°¡ CºÎÅÍ »ç¿ëÇØ¿Â °ÍÀÌ´Ù.
±×¿¡ ºñÇØ¼­ Integer´Â Å¬·¡½º·Î ÀÚ¹Ù¿¡¼­ »ç¿ëÇÏ°Ô µÈ °ÍÀÌ´Ù.
ÀÌ¹Ì Á¸ÀçÇÏ´Â int¸¦ Integer·Î ¸¸µç°ÍÀº ÆíÀÇ¼ºÀ» Á¦°øÇÏ±â À§ÇØ¼­
ÀÎµ¥ Integer¸¦ »ç¿ëÇÏ¸é null°ª Ã³¸®°¡ ¿ëÀÌÇØ¼­ sql°ú ¿¬µ¿ÇÒ
°æ¿ì Æí¸®ÇØÁø´Ù.

###GitÀÇ »ç¿ë¹ý
GitÀÌ¶õ?
¼ÒÇÁÆ®¿þ¾îÀÇ ¹öÀüÀ» °ü¸®ÇÏ±â À§ÇÑ ¼ÒÇÁÆ®¿þ¾î·Î ¼Ò½ºÄÚµå°¡
º¯°æµÈ ÀÌ·ÂÀ» ½±°Ô È®ÀÎÇÒ ¼ö ÀÖ°í Æ¯Á¤ ½ÃÁ¡¿¡ ÀúÀåµÈ ¹öÀü°ú
ºñ±³µµ °¡´ÉÇÏ°í Æ¯Á¤ ½ÃÁ¡À¸·Î º¹¿øÇÒ ¼ö ÀÖ´Ù.
Æ¯Â¡À¸·Î´Â ºü¸¥¼Óµµ¿¡ ´Ü¼øÇÑ ±¸Á¶ ¿Ïº®ÇÑ ºÐ»ê°ú ºñ¼±ÇüÀûÀÎ 
°³¹ßÀÌ ÀÖ´Ù.

°ü¸® ½Ã½ºÅÛ Á¾·ù
1. Áß¾Ó ÁýÁß½Ä ¹öÀü °ü¸® ½Ã½ºÅÛ(CVCS : Centralized VCS)
¼­¹ö ÇÏ³ª¿¡ ÁýÁßµÇ´Â ÇüÅÂ·Î °ü¸®ÇÏ±â°¡ ¹«Ã´ ´Ü¼øÇÏÁö¸¸
¼­¹ö°¡ °íÀå³ª¼­ µ¥ÀÌÅÍ°¡ »ç¶óÁö¸é ÄÚµå ÀÚÃ¼°¡ ³¯¶ó°¡
º¹¼ö°¡ ¾ÆÁÖ Èûµé´Ù.
2. ºÐ»ê ¹öÀü °ü¸® ½Ã½ºÅÛ(DVCS : Distributed VCS)
¿©·¯±ºµ¥¿¡ ºÐ»êÇÏ¿© ÀúÀåµÇ°í °³ÀÎ¸¶´Ù ÀúÀå¼Ò°¡ ÀÖ¾î
¼­¹ö¿¡ Á¢¼ÓÇÏÁö ¾Ê¾Æµµ °³¹ßÀÌ °¡´ÉÇÏ´Ù.

GitÀÇ ÀÛ¾÷ Èå¸§
1. ÀÛ¾÷È¯°æ¿¡¼­ ÄÚµå¸¦ ¿Ï¼º
2. ¿Ï¼ºµÈ ÄÚµå¸¦ ÀÚ½ÅÀÇ ÀúÀå¼Ò¿¡ Ä¿¹Ô
3. ÀÚ½ÅÀÇ ÀúÀå¼Ò¿¡ Ä¿¹ÔµÈ ³»¿ëÀ» ¼­¹ö¿¡ Çª½Ã
4. Çª½ÃµÈ ÄÚµå´Â »õ ¹öÀüÀ¸·Î ÀúÀåµÊ.

Master¿Í Branch
Master´Â ÇöÀç ¼­¹ö¿¡ ¿Ã·ÁÁ® ÀÖ´Â ¿ÏÀüÇÏ°Ô È®ÀÎµÈ ÄÚµåÀÌ¸ç
Branch´Â ÀÛ¾÷À» À§ÇØ ÇØ´çµÇ´Â ±¸¿ª¸¸À» °³ÀÎ ÀúÀå¼Ò·Î °¡Á®¿À¸ç
ÄÚµå¸¦ ´Ù ÀÛ¼ºÇÑ ÈÄ¿¡ ¼­¹ö¿¡ ¿Ã¸®¸é °ËÅä ÈÄ ¹®Á¦ ¾øÀ» ½Ã¿¡
MasterÀÇ ÄÚµå¿Í ÇÕÃÄÁØ´Ù.


####¸®´ª½º Ä¿³Î
1. ¸®´ª½º Ä¿³ÎÀÌ¶õ ¸®´©½º Åä¹ßÁî¸¦ À§½ÃÇÑ ¼¼°è °¢ÁöÀÇ °³¹ßÀÚ¿¡ 
ÀÇÇØ °³¹ßµÇ°í ÀÖ´Â ¸®´ª½º¸¦ ¶æÇÑ´Ù.

¸®´ª½º Ä¿³ÎÀº ¸»±×´ë·Î Ä¿³Î¸¸ ÀÖ±â ¶§¹®¿¡ ÀÌ°Í¸¸À¸·Î´Â ¾Æ¹«°Íµµ
ÇÒ ¼ö°¡ ¾ø´Ù. ÀÌ Ä¿³Î¿¡ °¢ °³¹ß ¾÷Ã¼µéÀÌ ÄÄÆÄÀÏ·¯, ÆíÁý±â, 
À¥ºê¶ó¿ìÀúµî°ú °°Àº ÀÀ¿ë ¾îÇÃ¸®ÄÉÀÌ¼ÇÀ» Ãß°¡ÇØ¼­ ¸¸µç °ÍÀ»
¸®´ª½º ¹èÆ÷ÆÇÀÌ¶ó°í ÇÑ´Ù.

2. ¸®´ª½º Ä¿³Î ¹öÀüÀº linux-2. 4. 18°°Àº Çü½ÄÀÎµ¥ Á¦ÀÏ ¾ÕÀÇ ¼ýÀÚ´Â
¸ÞÀÌÀú ¹öÀüÀ¸·Î Ä¿³ÎÀÇ ±¸Á¶³ª ±â´É¿¡ ±Þ°ÝÇÑ º¯È­°¡ ÀÖÀ» ¶§
¹Ù²î¸ç µÎ¹øÂ° ¼ýÀÚ´Â ¸¶ÀÌ³Ê ¹öÀüÀ¸·Î ³»ºÎ±¸Á¶¸é¿¡¼­ ¸¹Àº
º¯È­°¡ ÀÖÀ» ¶§ ¹Ù²î´Â ¹öÀüÀÌ´Ù. ¶Ç ¸¶ÀÌ³Ê ¹öÀüÀÌ Â¦¼öÀÏ¶§´Â
¾ÈÁ¤µÈ Ä¿³Î ¼Ò½ºÀÓÀ» ³ªÅ¸³»°í È¦¼öÀÏ¶§´Â ¾ÆÁ÷ °³¹ßÁßÀÎ ¹öÀüÀ»
³ªÅ¸³½´Ù.

3. À¯´Ð½º ½Ã½ºÅÛÀÇ ´ëÇ¥ÀûÀÎ Æ¯Â¡ Áß¿¡ ÇÏ³ª´Â user mode¿Í 
kernel mode°¡ ³ª´²Á® ÀÖ´Ù´Â °ÍÀÎµ¥ ¸®´ª½º ¿ª½Ã À¯´Ð½º¸¦ ¸ðµ¨·Î 
¸¸µé¾îÁ® ÀÖ¾î ÀÌ¸¦ µû¸¥´Ù.
- Kernel mode Æ¯±Ç¸ðµå·Î ¸ðµç ÁÖ¼Ò°ø°£¿¡ Á¢±ÙÀÌ °¡´ÉÇÏ°í ¸ðµç
¸í·ÉÀ» ¼öÇàÇÒ ¼ö ÀÖ´Ù.
- user mode À¯Àú¸ðµå·Î ÀÚ½Å¿¡°Ô ÇÒ´çµÈ ÁÖ¼Ò °ø°£¸¸ Á¢±ÙÇÒ 
¼ö ÀÖ°í Kernel modeÀÇ ÁÖ¼Ò °ø°£¿¡ ´ëÇØ¼­´Â Á¢±ÙÀÌ ºÒ°¡´ÉÇÏ´Ù.
¶ÇÇÑ ½Ã½ºÅÛ¿¡ Ä¡¸íÀûÀÎ ¿µÇâÀ» ³¢¯‚ ¼ö ÀÖ´Â Æ¯±Ç ¸í·ÉÀº
»ç¿ëÀÌ ºÒ°¡´ÉÇÏ´Ù.(lgdt, lidt, cli, stiµî)

System Call Interface´Â user mode ÇÁ·Î¼¼½ºÀÎ ÀÀ¿ë ¾ÖÇÃ¸®ÄÉÀÌ¼ÇÀÌ
Ä¿³ÎÀÇ ±â´ÉÀ» »ç¿ë °¡´ÉÇÏ°Ô ÇØÁØ´Ù. ½Ã½ºÅÛ ÄÝÀ» »ç¿ëÇÏ¸é
Ä¿³Î ¸ðµåÀÇ ÇÔ¼ö³ª ÀÚ·á ±¸Á¶¿¡ Á¢±ÙÇÒ ¼ö ÀÖ°Ô µÈ´Ù´Â ¸»ÀÌ´Ù.

4. Memory Management´Â ½Ã½ºÅÛ¿¡ ÀÖ´Â ¸Þ¸ð¸® ÀÚ¿øÀ» °ü¸®ÇÏ´Â
ºÎºÐÀ¸·Î¼­ ¸®´ª½º´Â ¸Þ¸ð¸® °ü¸® ¾Ë°í¸®ÁòÀ¸·Î buddy slabÇÒ´çÀÚ¸¦
»ç¿ëÇÑ´Ù.

5. Task Management´Â ÅÂ½ºÅ©¸¦ °ü¸®ÇÏ´Â ºÎºÐÀÌ´Ù.
(ÅÂ½ºÅ©´Â ÀÚ¿ø ¼ÒÀ¯±ÇÀÇ ´ÜÀ§ÀÌ´Ù) 
±¸Ã¼ÀûÀ¸·Î´Â ÅÂ½ºÅ©ÀÇ »ý¼º,¼Ò¸ê,Áß´Ü µîÀ» ´ã´çÇÑ´Ù.

6. IPC(InterProcess Communication)´Â °¡»óÁÖ¼Ò¸¦ »ç¿ëÇØ¼­ 
ÇÁ·Î¼¼½º°£ Åë½ÅÀ» ´ã´çÇÏ´Â ºÎºÐÀÌ´Ù. ÀÌ¶§ ÆäÀÌÂ¡ ±â¹ýÀ»
»ç¿ëÇÏ´Âµ¥ ÀÌ·Î½á ÁÖ¼Ò°ø°£À» ºÐ¸®ÇÏ¿© ´Ù¸¥ ÇÁ·Î¼¼½ºÀÇ
ºñÁ¤»óÀûÀÌ°Å³ª ¾ÇÀÇÀûÀÎ ¼öÇàÀ¸·ÎºÎÅÍ º¸È£¸¦ ÇÏ°í ¾ÖÇÃ¸®ÄÉÀÌ¼ÇÀ»
ÄÄÆÄÀÏÇÒ ¶§ ¼öÇà À§Ä¡¿¡ ´ëÇØ¼­ °í¹ÎÇÏÁö ¾Ê¾Æµµ µÈ´Ù´Â µîÀÇ
ÀåÁ¡À» °¡Áö°Ô µÈ´Ù.

7. VFS(Virtual File System)Àº °¢±â ´Ù¸¥ ÆÄÀÏ ½Ã½ºÅÛ, µð¹ÙÀÌ½º¿¡
´ëÇØ¼­ open,read,write,closeµî°ú °°Àº µ¿ÀÏÇÑ ÀÎÅÍÆäÀÌ½º¸¦
»ç¿ëÇÒ ¼ö ÀÖ°Ô ÇØÁØ´Ù.
VFS·Î ÀÎÇØ¼­ ¸®´ª½º´Â ¿©·¯ ÆÄÀÏ ½Ã½ºÅÛÀ» »ç¿ëÇÒ ¼ö ÀÖ°Ô µÇ¾ú°í
¿©·¯ ¿î¿µÃ¼Á¦¿Í ÇÔ²² °øÁ¸ÇÏ¸ç ÀÌ·¸°Ô ¼ºÀåÇÒ ¼ö ÀÖ°Ô µÇ¾ú´Ù.
 
8. BSD Socket Interface´Â bind,connect,accept,send,recvµîÀ¸·Î
´ëº¯µÇ´Â BSD socket interface¸¦ Á¦°øÇÑ´Ù.

9. File StstemÀº ext2,ext3,vfat,jfsµîÀÇ ÆÄÀÏ ½Ã½ºÅÛÀ» Á¦°øÇÑ´Ù.

10. Network Protocol StackÀº ipv4,ipv6,atm,x25¿Í °°Àº
ÇÁ·ÎÅäÄÝ ½ºÅÃÀ» °¡Áö°í ÀÖ´Ù.

11. Device Driver´Â ÇÏµåµð½ºÅ©, Å°º¸µå, ¸¶¿ì½º µîÀÇ µð¹ÙÀÌ½º
µå¶óÀÌ¹ö¸¦ Æ÷ÇÔÇÏ°í ÀÖ´Â ºÎºÐÀÌ´Ù.


#####Å©·Î½º ÄÄÆÄÀÏ
Å©·Î½º ÄÄÆÄÀÏÀº ½ÇÇàµÇ´Â ÇÃ·§ÆûÀÌ ¾Æ´Ï¶ó ´Ù¸¥ ÇÃ·§Æû¿¡¼­µµ
½ÇÇà °¡´ÉÇÑ ÄÚµå¸¦ ¸¸µå´Â °ÍÀ» ¶æÇÑ´Ù.



 