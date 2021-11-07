# CC-CV_Adjustable_Buck_Converter
![](https://github.com/mustafasenel/CC-CV_Adjustable_Buck_Converter/blob/main/rendered_images/1.jpeg?raw=true)
## Schematic
![](https://github.com/mustafasenel/CC-CV_Adjustable_Buck_Converter/blob/main/Schematic.jpg?raw=true)

PS1, XL4016 denetleyici yongasıdır ve buck converter ana bileşenidir. XL4016, 8-36V giriş gerilimi, 1.25-32V ayarlanabilir çıkış gerilimine sahiptir ve 12A akım verebilmektedir.  D1, MBR20100 Schottky diyotu ve L2, buck converterin diğer temel bileşenleri olan bir 47uH-12A indüktörüdür. C6,C7,C8,C9 giriş, C1,C2,C3,C4 çıkış gürültülerini azaltmak için kullanılır. M1, güvenlik için kullanılmış 15A değerinde sigortadır. 

R2, çıkış voltajını ayarlamak için denetleyici yongasına bir feedback sağlayan 20K çok turlu bir trimpottur. C10, geri besleme yolundaki gürültüyü azaltmak için kullanılır. R9, çıkış akımını sınırlandırmak için kullanılan 500R değerinde bir trimpottur. Çıkış akımı sınırlandırıldığını görmek için D3 ledi kullanılmıştır. R4, 0.05R-5W değere sahip şönt direncidir. 

Devre üzerinde uzun süre yüksek akımlara karşı dayanıklılık sağlamak için opsiyonel olarak NTC fan devresi bulunmaktadır. Bu devre 10K NTC termistör (R11) ve IRLML2402 (IC2) mosfet ile oluşturulmuştur. R12 trimpotu sayesinde ayarlanan direnç ile istenilen sıcaklık seviyesinde mosfet tetiklenecek ve akım geçirmeye başlayacaktır. Bu sayede fanın kontrolü sağlanacatır.

U, kararlı bir +5V besleme sağlayan L7805CT2D lineer regülatör çipidir. C3 ve C11 regülatörün giriş ve çıkış gürültülerini azaltmak için kullanılmıştır. Bu regülatör ile MCP6002 Opamp ve NTC fan devresine güç sağlanmaktadır. 

IC1, PS1'in feedback pinini tetiklemek için küçük şönt direnç voltajını yükseltmek için kullanılan MCP6002 opamptır. D2, PS1'e bir feedbacksağlar. MCP6002 yongası içerisinde iki opamp bulundurmaktadır. İlk opamp, evirmeyen yükselteç olarak kullanılır ve ikinci opamp, D3 ve D4 LED'lerini (CC, CC) beslemek için bir karşılaştırıcı olarak yapılandırılır. R6, C14,C15,C16 besleme gürültüsünü azaltmak için kullanılmıştır. R10 ve C17 ayrıca şönt seslerini ortadan kaldırmak için kullanılmıştır. C12 ayrıca yükselteç giriş gürültüsünü azaltmak için kullanılır.
## PCB
![](https://github.com/mustafasenel/CC-CV_Adjustable_Buck_Converter/blob/main/PCB_print_color.jpg?raw=true)

Kaynaklar

https://www.pcbway.com/blog/technology/0_30V__0_7A_Adjustable_Switching_Power_Supply.html
http://www.xlsemi.com/datasheet/xl4016%20datasheet.pdf
