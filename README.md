<a name="br1"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

รายงานสรปผลการฝกทกษะวจย

เยาวชนโครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจยของศนยวจยแหงชาต สวทช.

1\. หวขอการฝกทกษะวจย

การฝกทกษะวจยเกยวกบการคดแยกระดบการควของกาแฟดวยเทคนคสเปกโทรสโกปรวมกบ Machine Learning และ

ꢂ

การเกบและจดการขอมล 3D ดวยเทคโนโลย LiDAR แบบพกพา

2\. ผเขารบการฝกทกษะวจย

นายกตตพงศ เทพอย

กำลงศกษาชนปท 2 ภาควชาวศวกรรมคอมพวเตอร คณะวศวกรรมศาสตร มหาวทยาลยเทคโนโลยพระจอมเกลาธนบร

3\. รายชอนกวจยพเลยง

ดร.รงโรจน จนตเมธาสวสด

ทมวจย เทคโนโลยเทระเฮรตซ

กลมวจย อปกรณสเปกโทรสโกปและเซนเซอร

ศนย เทคโนโลยอเลกทรอนกสและคอมพวเตอรแหงชาต (NECTEC)

4\. ระยะเวลาการฝกทกษะวจย

เรมตน วนท 19 เดอน มถนายน พ.ศ. 2566

สนสด วนท 4 เดอน สงหาคม พ.ศ. 2566

รวมระยะเวลาฝกทกษะวจย 35 วน

5\. ขอมลเกยวของหองปฏบตการวจยทนกเรยนเขารบการฝกทกษะวจย

เปนหองปฏบตการทมการศกษาวจยในหลาย ๆ ดาน เชน 1) งานดาน Spectroscopy โดยไดนำเทคโนโลยนไปประยกต

กบงานอน ๆ ตวอยางคอ การนำไประบระดบการควของกาแฟ 2) งานดาน LiDAR เปนการนำเทคโนโลยดงกลาว ไปเกบภาพ

โบราณสถานตาง ๆ ภายในประเทศไทย เพอตอยอดงานทางโบราณคด 3) งานการพฒนา Web Application ซงไดจดทำเพอจดเกบ

ขอมลตาง ๆ คอ ขอมล Spectrum เปนตน 4) งานดานการพฒนา GUI สำหรบนำไปใชบนเครองมอตรวจวดเชอราทรวมพฒนากบ

ศนยพนธวศวกรรมและเทคโนโลยชวภาพแหงชาต (BIOTEC) เปนตน โดยไดรบมอบหมายใหรบผดชอบในหวขอ การคดแยกระดบ

การควของกาแฟ และสนบสนนงานในหวขอการจดเกบขอมลโบราณสถานดวยเทคโนโลย LiDAR แบบพกพา



<a name="br2"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

6\. สรปการปฏบตงานโดยสงเขป

1\. การประมวลผล Raman Spectrum จากขอมลตวอยางระดบการควกาแฟ

เปนการนำขอมล Raman Spectrum ของกาแฟทผานการควในแตละระดบ โดยใช Machine Learning เพอทำนายหา

ระดบการคว ซงม เขม กลาง ออน ซง Raman Spectrum ของการควแตละระดบจะมเอกลกษณทแตกตางกนไป กลาวคอ ความ

เขม (Intensity) ในแตละ Wave Number จะแตกตางกน ในขนตอนการทำงานมขนตอนแตกตางกนดงตอไปน

1\.1) Data Exploration

ขอมลทไดรบเปนขอมลสเปกตรม (Spectrum) ทผานการตรวจวดจากโดยใชเทคนคของ Raman Spectroscopy ซงขอมล

ทไดรบจะอยในรปแบบของ csv file ดงรปท 1 ซงจะประกอบไปดวย X, Y, Wave (Wave Number), Intensity และ

Level

รปท 1 รปตวอยางขอมล Spectrum

จากขอมลตวอยางขางตนเมอนำมาเขยนในรปของกราฟ โดยให แกน X คอ Wave Number และ แกน Y คอ Intensity

ไดกราฟดงรปท 2 โดยแกน Y แทนคาของ Intensity (a.u.) และแกน X แทน Wave Number (cm<sup>-1</sup>) ซงแสดงตวอยาง

ของสเปกตรมจำนวน 50 เสน จะพบวามเสนทเชอมโยงในแตละเสนตามลกศรสแดง ซงเกดจาก library ของ python ทชอ

วา matplotlib เนองจากในการ plot จดแตละจุด plot function ทใชในการ plot จะทำการวาดกราฟโดยทำการเชอม

จดแตละจดเขาดวยกน ทำใหเมอเปลยนเสนสเปกตรม จดเรมตนของเสนสเปกตรมแรก จะเกดเสนเชอมกบ จดสดทายกบ

สเปกตรมของเสนกอนหนา ซงตองแกปญหาโดยการหาวาในแตละสเปกตรมมจดกจดเปนองคประกอบ



<a name="br3"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

รปท 2 ตวอยางสเปกตรมจากขอมล csv จำนวน 50 ตวอยาง

โดยแกน Y แทนคาของ Intensity (a.u.) และแกน X แทน Wave Number (cm<sup>-1</sup>)

ในการหาจำนวนของจดทเปนองคประกอบของสเปกตรมนน ทำโดยการสมจำนวนจดเพอใหเกดเสนเชอม โดยจากการสม

พบวาตองใช 1013 จด จงจะเกดเสนเชอมไปยงสเปกตรมถดไป ดงรปตวอยางท 3 ดงนนทำใหไดขอสรปวาในสเปกตรม 1

เสนจะประกอบดวยจดจำนวน 1012 จด

รปท 3 (ซาย) กราฟสเปกตรมเมอมจำนวนจด 1013 จด (ขวา) กราฟสเปกตรมเมอมจำนวนจด 1012 จด

ข

ั

้

นตอนถ

ั

ดไปค

ื

อการเข

ี

ยนเลขสเปกตร

ั

มเพ

ื

่

อใช

ꢁ

ในการประมวลผลและสะดวกต

ꢃ

อการเร

ี

ยกใช

ꢁ

งาน โดยได

ꢁ

ทำการนำข

ꢁ

อม

ู

ล

ท

ั

้

งหมดไปหารด

ꢁ

วย 1012 จะได

ꢁ

จำนวนสเปกตร

ั

มท

ั

้

งหมด พบวาม หมด 906 สเปกตร

ꢃ

ี

ั

ง

ั

ม และสามารถระบ

ุ

สเปกตรมได

ั

ꢁ

ทำ

ใหไดตารางขอมลใหมดงรปท 4 ซง n\_spectrum เปน column ทเพมมา แทนหมายเลขของสเปกตรม

รปท 4 ตวอยางขอมลทงหมดทผานการระบหมายเลขของสเปกตรม

เมอผานขนตอนการระบเลขสเปกตรม นำมาวาดกราฟจะไดรปดงรปท 5 จะเหนวาไมเกดเสนทเชอมระหวางสเปกตรมแลว



<a name="br4"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

รปท 5 สเปกตรมตวอยางจำนวน 50 สเปกตรม ทผานการระบหมายเลขสเปกตรม

1\.2) Spike Removal

หลงจากผานขนตอนกอนหน

เรยกวา Spike ซงเกดจาก Cosmic Ray โดยพบได

เนองจากทำใหเมอนำสเปกตรมไปใชอาจจะเกดขอผ

สวนนเปนสวนเอกลกษณ ทำใหความถกตองในการทำนายลดลงได

ั

ꢃ

ั

้

ꢃ

ꢁ

าแล

ꢁ

ว เม

ื

่

อลองแสดงสเปกตร

วไปจากการว

ดพลาดในการต

ั

มพบว

ꢃ

าม

ดสเปกตร

ความสเปกตร

ี

บางสเปกตร

ม ซงจำเป

ม เช

ั

มท

ี

่

ม

ꢅ

ี

เส

นต

น machine learning อาจค

ꢁ

นท

ี

่

ลากแสดงข

ั

้

นมา ด

ั

งร

ู

ปท

ี

่

6

ม

ี

ꢃ

ึ

่

ิ

ꢁ

ท

ิ

ั

่

ั

ั

ึ

่

ꢁ

องลบส

ꢃ

วนนออกจากสเปกตร

ี

้

ั

ื

่

ꢁ

ื

่

ั

ꢁ

ิ

ꢁ

ี

ั

ꢃ

ิ

ดว

ꢃ

า

รปท 6 สเปกตรมระดบกลาง เสนท 331

ขนตอนการลบ Spike คอเทคนคทเรยกวา Spike removal ทำไดหลายวธ โดยวธทเลอกใชคอการประยกตใชเทคนค

Modified Z score [1] ซง Z score เปนตวเลขทางสถต คำนวณไดจาก

(ꢂ − ꢃ)

ꢀ =ꢁ

ꢄ

ꢂꢁ: Data point (Intensity ณ ตำแหนงตางๆ ของสเปกตรม), ꢃꢁ: Mean, ꢄ : Standard Deviation

นำ Z score ทไดมาวาดกราฟ จากนนกำหนดคา Threshold เพอเปนเกณฑในการระบวา สวนไหนมความเปนไปไดทจะ

เปน Spike อางองจากสวนทสเปกตรมตดผานเสน Threshold โดยในตวอยางน Threshold มคาเทากบ 4 ดงรปท 7 (ซาย)

จากนนทำการตรวจสอบวาคา Z score สวนไหนบางทมคามากกวา Threshold จะไดดงรปท 7 (ขวา) จะสงเกตไดวามแทง

[1] N. Coca, "Removing Spikes from Raman Spectra with Anomaly Detection: Whitaker-Hayes algorithm in Python," 20 November 2019. [Online]. Available:

https://towardsdatascience.com/removing-spikes-from-raman-spectra-8a9fdda0ac22. [Accessed 10 August 2023].



<a name="br5"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

ปรากฏขนมาจำนวน 3 แทง เหมอนการทำภาพตดขวางของสเปกตรม โดยกราฟนจะเปนกราฟทมเพยง 1 และ 0 เทานน 1

คอจดทเสน Threshold ตดผาน และ 0 คอจดทไมมการตดผานของเสน Threshold ในเสนสเปกตรม

รปท 7 (ซาย) กราฟ Z Score ทไดจากสเปกตรม (ขวา) เสนกำกบ Threshold

เม

(ขวา) ซ

Threshold ม

จะไดสเปกตรมท

สเปกตรม

ื

ꢁ

ꢃ

ี

ั

ั

ꢁ

ั

็

ื

ꢃ

ꢃ

ี

เ

ป

ꢅ

ู

ꢁ

ꢃ

ู

ี

7

น

ึ

่

ู

วแปร m ในกรณ

ี

น

ี

้

ได

ꢁ

เล

ื

อกใช

ꢁ

ꢃ

าถ

ꢁ

าหากส

ꢃ

วนใดของกราฟท

ꢁ

างมากกว

ꢃ

า 7 หน

ꢃ

วย จะทำการต

ั

ดออกและนำค

ꢃ

าหล

ั

งจากตำแหน

ꢃ

งน

ั

้

นระยะ -7 ถ

ั

งรปท 8 โดยส

ู

ี

่

ꢃ

วนสแดงคอสวนท

ี

ื

ꢃ

ี

่

เคยเป

ꢅ

น Spike ในสเปกตร

ั

ม น

รปท 8 สเปกตรมทผานการลบ Spike

1\.3) Baseline Removal

จากรปท 5 จะพบวาสเปกตรมแต

เรยกวา Baseline Removal ซงทำได

โดยมใหเลอกหลายว ในกรณ เลอกใช

สเปกตรมทกเสนนนมฐานในตำแหนงเดยวกนแลว

ู

ี

่

ꢃ

ั

ꢃ

ละเส

โดยการเร

โมเดล drPLS เม

ꢁ

นท

ี

่

ฐานท

ี

่

ยกส

ู

งไม

Library ท

อลบท

ꢃ

เท

ꢃ

าก

ั

น จงจำเปนตองทำใหฐานของแตละเสนเทากน ในขนตอนน

เรยกวา Rampy ซงม Function สำหรบลบ Baseline

กสเปกตรมแลวจะไดผลปรากฏดงรปท 9 เหนได

ี

ꢃ

ึ

่

ꢁ

ี

ยกใช

ꢁ

ี

่

ี

ꢃ

ึ

่

ี

ั

ี

ꢁ

ื

ิ

ธ

ี

ี

น

ี

้

ื

ꢁ

ื

่

ุ

ั

ꢁ

ꢁ

ั

ู

ี

่

็

ꢁวꢃา



<a name="br6"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

รปท 9 การเปรยบเทยบผลลพธหลงจากการลบ Baseline ในแตละระดบการคว

ทระดบ เขม สนำเงนแทนสเปกตรมทยงไมผานการลบ Baseline และ สแดงแทนสเปกตรมทถกลบ Baseline

ทระดบ ออน สเขยวแทนสเปกตรมทยงไมผานการลบ Baseline และ สนำเงนแทนสเปกตรมทถกลบ Baseline

ทระดบ กลาง สแดงแทนสเปกตรมทยงไมผานการลบ Baseline และ สเขยวแทนสเปกตรมทถกลบ Baseline

1\.4) Removing noisy data by using derivative technique

หล

(noise) ด

การเปลยนแปลง (Derivative) มาช

การเปลยนแปลงตลอดเวลา ด

อยตดกนไดจากสมการ

ั

งจากท

ี

่

สเปกตร

ั

มม

ี

ฐานท

ี

่

เท

ꢃ

าก

าสเปกตร

วยในการค

ั

นแล

ꢁ

ว ส

ิ

่

งท

ี

ั

่

้

ต

ꢁ

องทำในข

น มเสนขรขระจำนวนมาก ซ

ดกรองสวนนออกไปได จากต

ั

้

นตอนถ

ั

ดมาค

ื

อการลบส

งในทางคณ

วอยางพบว

ꢃ

วนท

ี

่

ม

ิ

ี

การเปล

ตศาสตร

า มเสนท

ี

่

ꢄ

ยนแปลงในสเปกตร

นเราสามารถประย

นลงถมากๆ ทำให

ัมเยอะ

ั

งร

ู

ปท 10 จะเห

ี

่

็

นได

ꢁ

ว

ꢃ

ั

มน

ี

ꢁ

ุ

ึ

่

น

ั

้

ุ

กต

ꢄ

ใช

ꢁ

ี

่

ꢃ

ั

ꢃ

ี

้

ꢁ

ั

ꢃ

ꢃ

ี

ꢁ

ี

่

ข

ึ

้

ี

่

ꢁ

เก

ิด

ี

่

ั

งนนจะเรมไดโดยการหาการเปลยนแปลงของกราฟในแตละคของคาความเขมในสเปกตรมท

∆ꢆ

ꢅ =ꢁ

∆ꢂ

นมารวมก

เม

ื

่

อได

ꢁ

ค

ꢃ

าการเปล

ี

่

ยนแปลงหร

ื

อความช

ั

นแล

ꢁ

ว ก

็

นำค

ꢃ

าเหล

ꢃ

าน

ั

้

ั

น จะได

ꢁ

เป

ꢅ

นผลรวมค

ꢃ

าการเปล

ี

่

ยนแปลงท

ั

้

งหมดใน

สเปกตรมนนดงสมการ เมอ N คอขนาดของสเปกตรมเสนนนๆ

ꢁꢂꢃ

ꢇꢈꢅ =ꢁ ꢉ |ꢅ<sub>ꢀ</sub>|

ꢀꢄꢃ

หล

การเปลยนแปลงทเหมาะสม ซ

ไหน จะทำใหกราฟมความเรยบมากท

ใหกราฟเรมไมมความเรยบ จงทำการคดกราฟนนออกจากขอมลทสามารถใชได

ั

งจากคำนวณผลรวมการเปล

ี

่

ยนแปลงท

า Threshold สามารถทำได

ด พบวาในตวอยางขอม

ั

้

งหมดในสเปกตร

ั

มแต

ꢃ

ละเส

ꢁ

นแล

าเม

หากผลรวมค

ꢁ

ว ก

็

จะทำการหาค

ꢃ

า Threshold ของผลรวมค

ꢃ

า

ꢃา

ึ

่

งค

ꢃ

ꢁ

โดยการหาว

ꢃ

ื

่

อผลรวมค

ꢃ

าการเปล

ี

่

ยนแปลงม

ี

ค

ꢃ

าน

ꢁ

อยกว

ꢃ

าค

ꢁ

ี

ี

ี

่

ส

ุ

ꢃ

ั

ꢃ

ꢁ

ู

ลน

ี

้

ꢃ

าการเปล

ี

่

ยนแปลงม

ี

ค

ꢃ

ามากกว

ꢃ

า 30 จะทำ



<a name="br7"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

รปท 10 ตวอยางของกราฟทมความขรขระ (noise เยอะ)

1\.5) Smoothing graph by using savgol\_filter from Scipy

ในกรณ สเปกตรมถกคดออกแลวจากขนตอนกอนหนา สเปกตรมท าผลรวมอ

ความเปนไปได จะเปนสเปกตรมท noise เยอะ ดงนนเราสามารถทำให

savgol\_filter function ใน Scipy Module โดยในคำสงจำเปนตองมการเลอก polyorder และ mode ซงในขอมลน

าทเหมาะสมคอ polyorder = 3 และ mode = “nearest” ทำใหไดผลลพธ งรปท 11 สเปกตรมสแดงคอสเปกตรมท

งไมได านการทำใหเรยบ และเสนส ำเงนคอสเปกตรมท านกระบวนการทกลาวมาแลว เหนได าสเปกตรมส ำเงนมี

ี

ท

ี

่

ั

ู

ั

ꢁ

ั

้

ꢃ

ꢁ

ั

ี

่

ม

ี

ค

ꢃ

ั

ตราการเปล

ี

่

ยนแปลงน

ꢁ

อยกว

ꢃ

า 30 ก

็ยังมี

ꢅ

ꢁ

ท

ี

่

ꢅ

ั

ี

่

ม

ี

ั

ั

้

ꢁ

สเปกตรมม

ั

ี

ความเรยบได

ี

ꢁ

โดยการใชꢁ

ั

่

ꢅ

ꢁ

ี

ื

ค

ꢃ

ี

่

ื

ꢁ

ꢁ

ั

ꢄ

ด

ั

ู

ี

่

ย

ั

ꢃ

ꢁ

ผ

ꢃ

ꢁ

ี

ꢁ

ี

น

้

ิ

ื

ั

ี

่

ผ

ꢃ

ี

่

ꢃ

ꢁ

็

ꢁ

ว

ꢃ

ั

ี

น

้

ิ

ความเรยบมากขน

รปท 11 สเปกตรมทม noise เยอะ (แดง) และสเปกตรมทผานการทำใหเรยบ (นำเงน)

1\.6) Rescaling

รปท 12 ตวอยางสเปกตรมทมอตราสวนทแตกตางกน



<a name="br8"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

จากรปท 12 ดายซายจดยอดทสงทสดของสเปกตรมมคาประมาณ 10,000 หนวย แตดานขวามคาสงสดประมาณ 3,600

หนวย ซงเมอดภาพรวมของขอมลแลวพบวาคาความสงของจดยอดนนตางกนมากเกนไปจงจำเปน

ꢅ

ตองทำการรบความเขม

ของทกสเปกตรมใหมความใกลเคยงกน ซงทำไดโดยเรมจากการหาอตราสวนตอ 1 หนวย ทหาได

ꢁดงสมการ

1

<sup>ꢅꢆꢇꢈꢉꢊꢋꢈꢇꢌ</sup><sub>!"#$%&'(</sub> =ꢉ<sub>|maxꢀ(ꢁꢂꢃꢄꢂꢅꢆꢃꢇ)ꢀꢁꢂꢃꢄꢅꢆꢇ</sub>

(

)

ꢀꢁꢂꢃꢄꢅꢆꢇ

|

ꢀ− min ꢁꢂꢃꢄꢂꢅꢆꢃꢇ

เมอ Unit Ratio<sub>spectrum</sub>

ค

ื

ออ

ั

ตราส

ꢃ

วน 1 หน

ꢃ

วยของสเกตร

ั

ม โดยสเปกตร

ั

มอ

ื

่

น ๆ จะม

ี

ความแตกต

ꢃ

างก

ั

นมาก ทำให

ꢁ

ต

ꢁ

องม

ีการ

เปลยนความเขม ของทกสเปกตรมใหมคาคลายคลงกน ดงสมการ

(ꢄꢅꢆꢁꢅꢇꢈꢆꢉ<sub>ꢀ</sub>)<sub>ꢁꢂꢃꢄꢅꢆꢇꢈ</sub>

ꢊꢋꢅꢈꢆꢃꢌꢍꢆꢈꢎ<sub>ꢁꢂꢃꢄꢅꢆꢇꢈ</sub>ꢏ<sup>ꢉꢊ</sup>

(ꢀꢁꢂꢃꢄꢅꢆꢁꢅꢇꢈꢆꢉ<sub>ꢀ</sub>)<sub>ꢁꢂꢃꢄꢅꢆꢇꢈ</sub> =ꢃ

∗ | max(ꢄꢅꢆꢁꢅꢇꢈꢆꢉ)<sub>ꢆꢃꢋ\_ꢁꢂꢃꢄꢅꢆꢇꢈ</sub> − min(ꢄꢅꢆꢁꢅꢇꢈꢆꢉ)<sub>ꢆꢃꢋ\_ꢁꢂꢃꢄꢅꢆꢇꢈ</sub>

|

เมอ ref\_spectrum คอ สเปกตรมอางองทตองการใชปรบสเปกตรมอนใหมความเขมคลายคลงกนทำให

อตราสวนเทากนในทกเสน แสดงดงรปท 13

ꢁไดกราฟทม

รปท 13 สเปกตรมทกเสนทมอตราสวนเทากน ตามระดบการคว

1\.7) Machine Learning Process

เมอไดขอมลทงหมดพรอมสำหรบการเรยนรเพอทำนายแลว กทำการเทรนโมเดล โดยใช Pycaret Module ซงทำไดโดย

การใสขอมลเขาไป จากนน Pycaret จะทำการเทรนในทกโมเดล เพอหาโมเดลทดทสด ไดผลลพธแสดงดงรปท 14 ทำใหได

วามความถกตอง 77.89% และโมเดลทไดความถกตองมากทสดคอ Logistic Regression

รปท 14 ภาพประสทธภาพการทำนายผลของโมเดลตาง ๆ

เมอสงเกตจาก Confusion Matrix โดยท 0 แทนระการควเขม, 1 แทนระดบการควออน และ 2 แทนระดบการควกลาง ซงแกน Y คอระดบ

การควจรง และ X คอระดบการควทนำนายได พบวามการทำนายผดพลาดทกรณของการควเขมกบการควกลางเยอะกวากรณอน ดงรปท 15



<a name="br9"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

รปท 15 Confusion Matrix ของ Logistic Regression ทใชนำทายขอมลระดบการควของกาแฟ จาก Raman Spectrum

2\. การเกบภาพตวอยางโบราณสถาน โดยใช LiDAR Technology

ในการเกบภาพโบราณสถานดวยเทคโนโลย 3D นนมการเกบตวอย

การเกบโดยใช Terrestrial Laser Scanning (TLS) ซงไดรบมอบหมายในสวนของการเกบภาพดวย LiDAR บน iPhone โดยใน

การเกบตวอยางนนมการแบงการเกบเปน 2 สวนยอย คอ การเกบภาพตวอยางทงหมดในครงเดยว (Entire) และ การเกบแบบ

แยกสวน (Section) เชน ดานซาย ดานขวา และดานบน เปนตน แลวนำขอมลมารวมกน ซงเทคโนโลย LiDAR บน iPhone นน

สามารถเลอกระยะของการเกบ (Scanning Range) ได งแต 0.3 ถง 5.0 เมตร โดยขอบเขตและตวแปรในการเกบครงน อ 2,

3\.5 และ 5 เมตร จากนนเมอเกบขอมลแลว ในสวนของขอมลทแยกเกบจำเปนตองนำขอมลในแตละสวนมารวมกนโดยใช

อใหไดเปนโมเดล 3D ท ครบทกองคประกอบ โดยขอมลทไดออกมาจะม 2 ประเภทคอ PLY

็

ꢁ

ี

ั

้

ี

็

ั

ꢃางใน 2 รูปแบบคือ การเก็บโดยใชꢁ LiDAR บน iPhone และ

็

ั

ꢃ

ั

้

ี

ꢃ

็

ꢅ

ꢃ

ꢃ

ื

็

ั

ꢃ

ั

้

ั

้

ี

็

ื

็

ꢁ

ต

ั

้

ꢃ

ึ

ั

็

ั

้

ี้คื

ั

้

ื

่

็

ꢁ

ู

ꢁ

ꢃ

ꢁ

ู

ี

่

็

ꢅ

ꢁ

ꢁ

ู

ꢃ

ꢃ

ั

ꢁ

โปรแกรม CloudCompare เพ

ื

่

ꢁ

ꢁ

ꢅ

ี

่

ม

ี

ุ

ꢄ

ꢁ

ู

ี

่

ꢁ

ี

ื

และ FBX

2\.1) การเกบภาพโบราณสภานทจงหวดสพรรณบร

ในจงหวดน การเกบขอมล 2 ท อ เจด หมายเลข 3 และบานศรสรรเพชญ ซงแตละทกจะมรปแบบของสงปลกสรางท

แตกตางกน เชน บานศรสรรเพชญจะมลกษณะเปนสงปลกสรางทตำกวาพนดน เปนโพรงหลมดงรปท 16 โดยปญหาใน

ั

ั

ี

้

ม

ี

็

ꢁ

ู

ี

่

ค

ื

ียꢄ

ꢃ

ั

ꢃ

่

ꢃ

ื

้

ิ

ꢅ

ุ

ั

ู

ี

่

ꢆ

การเกบคอปรมาณแสง เนองจากเปนพนททถกสรางโดมครอบทบ ทำใหตองทำงานในเวลาทจำกด

รปท 16 โบราณสถานบานศรสนเพชรญ

เจด

กลางแจ

ทำงานของโปรแกรมทใชในการเกบขอมลทนท

ี

ย

ꢄ

หมายเลข 3 เปนเจดยอฐทม

ี

ฐานเป

ꢅ

นทรงส

ี

่

เหล

ี

่

ยม ม

ี

ฐานเป

ꢅ

นช

ั

้

นลำด

ั

บข

ั

้

นส

ู

งข

ั

้

นไป ด

ั

งร

ู

ปท

ี

่

17 เนองจากเปนสถานท

มากขน และจะหยดการ

ꢁ

งทำให องทำงานอยางเร

ꢁ

ต

ꢁ

ꢃ

ꢃ

งรีบเน

ื

่

องจากความร

ꢁ

อนของอากาศทำให

ꢁ

อ

ุ

ณภ

ู

ม

ิ

ของโทรศ

ั

พท

ꢄ

ึ

้

ุ



<a name="br10"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

รปท 17 เจดยหมายเลข 3 และภาพขณะเกบตวอยาง

หลงจากไดเกบตวอยางในแตละสถานท โมเดลทไดในแตละทจะมลกษณะดงรปท 18 และ 19

รปท 18 โมเดล 3D ของบานศรสรรเพชญทเกบดวย LiDAR บน iPhone โดยการเกบขอมลแบบ Entire

รปท 19 โมเดล 3D ของเจดยหมายเลข 3 ทเกบดวย LiDAR บน iPhone ทผานเกบแบบแยกสวน และประกอบแตละสวนเขาดวยกน

2\.2) การเกบภาพโบราณสภานทจงหวดราชบร

งานท

ี

่

ได

ꢁ

ร

ั

บมอบหมายค

ื

อการเก

็

บต

ั

วอย

ꢃ

างท

ี

่

จ

ั

งหว

ั

ดน

ี

้

ม

ี

2 ท คือ เจดียꢄหมายเลข 8 ซึ่งเปꢅนเจดียꢄที่มีลักษณะคลꢁายกับเจดียꢄ

ี

่

หมายเลข 3 ดงรปท 20 ซงทำใหเกบขอมลไดอยางความรวดเรว

รปท 20 เจดยหมายเลข 8 และภาพขณะวางแผนการเกบตวอยาง

โบสถ

ความแตกต

ทำอยางชา ๆ เพอใหไดรายละเอยดทครบถวน

ꢄ

ว

ั

ดโขลงส

ุ

วรรณค

ี

ร

ี

ซ

ึ

่

งได

ꢁ

มอบหมายให

ꢁ

ทำการแสกนท

ั

้

งภายในและภายนอกโบสถ

ꢄ

ซ

ี

ึ

่

งการเก

็

บต

ั

วอย

ꢃ

างในสถานท

ี

่

น

ี

้

ม

ี

ꢃ

างจากท

ี

่

อ

ื

่

นเน

ื

่

องจาก ม

ี

ความละเอ

ี

ยดท ากกวาเช

ี

ม

ꢃ

ꢃ

ิ

ั

ั

ู

21 เปนต

ꢅ

ꢁ

น ทำให

ꢁ

ในการเกบต

็

ꢁ

อง



<a name="br11"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

รปท 21 โบสถวดโขลงสวรรณคร ทงภายนอกและภายใน

หลงจากเกบภาพตวอยางครบแลว จงนำภาพแตละสวนมาประกอบทำใหไดโมเดลของสถานทตางๆ ดงรปท 22, 23

รปท 22 โมเดล 3D ของโบสถวดโขลงสวรรณคร ทงภายในและภายนอก ทเกบดวย LiDAR บน iPhone

ทผานเกบแบบแยกสวน และประกอบแตละสวนเขาดวยกน

รปท 23 โมเดล 3D ของเจดยหมายเลข 8 ทเกบดวย LiDAR บน iPhone โดยการเกบขอมลแบบ Entire

7\. การนำเสนอผลการฝกทกษะวจยของนกเรยนตอนกวจยพเลยง

7\.1) นำเสนอในรูปแบบ Scrum Meeting รꢃวมกับนักศึกษาคนอื่น ๆ ทุกเชꢁากꢃอนปฏิบัติงานในแตꢃละวันประมาณ 10 – 15

นาท

ี

7\.2) ทำ Power Point เพอนำเสนอผลการเกบขอมลภาพ 3D

7\.3) จดเกบ source code ไวใน Github Repository โดยสามารถ download หรอ git clone ไดใน

https://github.com/KittpongT/nectec\_internship

8\. ประโยชนทไดรบจากการเขารวมโครงการฝกทกษะวจย

ดานวชาการ : ไดรบความรเกยวกบ ธรรมชาตของ Spectrum และการใชประโยชนของ Spectrum ไดความรการจดการกบ

ขอมลประเภท Spectrum เชน การลบ Spike, Rescaling และ Graph Smoothing รวมไปถงทกษะดาน Machine Learning เพอ

ใชกบงานดาน Spectrum ไดรบความรเกยวกบเทคโนโลย LiDAR การเกบขอมล LiDAR และการจดการขอมล 3D ไดรบความร

เกยวกบอปกรณตาง ๆ ภายในทมวจย เชน Outdoor LiDAR เปนตน



<a name="br12"></a> 

โครงการรบนกเรยนระดบมธยมศกษาตอนปลาย/ครวทยาศาสตรฝกทกษะวจย

ณ หองปฏบตการวจย สวทช.

ดานอนๆ : ไดทกษะการใชชวตในองคกร ทงการพดคยกบนกวจย การทำงานเอกสาร การรบผดชอบตอเวลา ความรบผดชอบตอ

งานทไดรบ การอยรวมกบผอน ซงแตกตางกบการใชชวตในมหาวทยาลย

9\. ปญหาอปสรรคและแนวทางแกไข (ถาม)

บางคร

ั้งในการทำงานอาจจะไมꢃไดꢁมีความรูꢁมากพอ หรือติดกับปꢆญหาเปꢅนเวลานาน เชꢃน เทคนิคตꢃางๆเกี่ยวกับการจัดการ

ขอมล Spectrum โดยแกปญหาไดโดยการคนหาจากใน Internet และปรกษากบนกวจยพเลยง

10\. จะนำความร/ประสบการณทไดจากการเขารวมโครงการไปสอสารหรอประยกตใชอยางไร

ในการใชชวตในมหาวทยาลยจำเปนตองมทงความรและทกษะตาง ๆ เชนการแกปญหา ดงนน การทไดมาฝกทกษะวจยทน

ทำใหไดรบทกษะมากมาย อกทงยงสามารถนำไปตอยอดในการทำงานหลงจากจบมหาวทยาลยไดอกดวย เชน การพฒนางานจรง ๆ

ทเกดประโยชนเพอใหตอบโจทยผใชจรง

(ลงชอ)

ผฝกทกษะวจย

นกวจยพเลยง

(นายกตตพงศ เทพอย)

วนท

(ลงชอ)

(ดร.รงโรจน จนตเมธาสวสด)

วนท


