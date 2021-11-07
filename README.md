# CC-CV Adjustable Buck Converter
![](https://github.com/mustafasenel/CC-CV_Adjustable_Buck_Converter/blob/main/rendered_images/1.jpeg?raw=true)
## Schematic
![](https://github.com/mustafasenel/CC-CV_Adjustable_Buck_Converter/blob/main/Schematic.jpg?raw=true)

PS1, XL4016 denetleyici yongasıdır ve buck converter ana bileşenidir. XL4016, 8-36V giriş gerilimi, 1.25-32V ayarlanabilir çıkış gerilimine sahiptir ve 12A sabit akım verebilmektedir.  D1, MBR20100 Schottky diyotu ve L2, buck converterin diğer temel bileşenleri olan bir 47uH-12A indüktörüdür. C6,C7,C8,C9 giriş, C1,C2,C3,C4 çıkış gürültülerini azaltmak için kullanılır. M1, güvenlik için kullanılmış 15A değerinde sigortadır. 

R2, çıkış voltajını ayarlamak için denetleyici yongasına bir feedback sağlayan 20K çok turlu bir trimpottur. C10, geri besleme yolundaki gürültüyü azaltmak için kullanılır. R9, çıkış akımını sınırlandırmak için kullanılan 500R değerinde bir trimpottur. Çıkış akımı sınırlandırıldığını görmek için D3 ledi kullanılmıştır. R4, 0.05R-5W değere sahip şönt direncidir. 

Devre üzerinde uzun süre yüksek akımlara karşı dayanıklılık sağlamak için opsiyonel olarak NTC fan devresi bulunmaktadır. Bu devre 10K NTC termistör (R11) ve IRLML2402 (IC2) mosfet ile oluşturulmuştur. R12 trimpotu sayesinde ayarlanan direnç ile istenilen sıcaklık seviyesinde mosfet tetiklenecek ve akım geçirmeye başlayacaktır. Bu sayede fanın kontrolü sağlanacatır.

U, kararlı bir +5V besleme sağlayan L7805CT2D lineer regülatör çipidir. C3 ve C11 regülatörün giriş ve çıkış gürültülerini azaltmak için kullanılmıştır. Bu regülatör ile MCP6002 Opamp ve NTC fan devresine güç sağlanmaktadır. 

IC1, PS1'in feedback pinini tetiklemek için küçük şönt direnç voltajını yükseltmek için kullanılan MCP6002 opamptır. D2, PS1'e bir feedbacksağlar. MCP6002 yongası içerisinde iki opamp bulundurmaktadır. İlk opamp, evirmeyen yükselteç olarak kullanılır ve ikinci opamp, D3 ve D4 LED'lerini (CC, CC) beslemek için bir karşılaştırıcı olarak yapılandırılır. R6, C14,C15,C16 besleme gürültüsünü azaltmak için kullanılmıştır. R10 ve C17 ayrıca şönt seslerini ortadan kaldırmak için kullanılmıştır. C12 ayrıca yükselteç giriş gürültüsünü azaltmak için kullanılır.

******************************************************

PS1 is the XL4016 controller chip, and the buck converter is its main component. XL4016 has 8-36V input voltage, 1.25-32V adjustable output voltage and can give constant 12A current. D1 is the MBR20100 Schottky diode and L2 is a 47uH-12A inductor. It is used to reduce C6,C7,C8,C9 input, C1,C2,C3,C4 output noises. M1 is a 15A fuse used for safety.

R2 is a 20K multi-turn potentiometer that provides feedback to the controller chip to adjust the output voltage. C10 is used to reduce noise in the feedback path. R9 is a 500R trimpot used to limit the output current. D3 led is used to see that the output current is limited. R4 is the shunt resistor with a value of 0.05R-5W.

There is an optional NTC fan circuit on the circuit to provide resistance against high currents for a long time. This circuit is built with 10K NTC thermistor (R11) and IRLML2402 (IC2) mosfet. Thanks to the R12 potentiometer, the mosfet will be triggered at the desired temperature level with the adjusted resistance and will start to pass current. In this way, the control of the fan will be provided.

U1 is the L7805CT2D linear regulator chip that provides a stable +5V supply. C3 and C11 are used to reduce the input and output noise of the regulator. This regulator provides power to the MCP6002 Opamp and NTC fan circuit.

IC1 is the MCP6002 opamp used to amplify the small shunt resistor voltage to trigger the PS1's feedback pin. D2 provides a feedback to PS1. The MCP6002 chip contains two opamps. The first opamp is used as a non-inverting amplifier and the second opamp is configured as a comparator to feed the D3 and D4 LEDs (CC, CV). R6, C14, C15, C16 are used to reduce the supply noise. R10 and C17 were also used to eliminate shunt noises. C12 is also used to reduce amplifier input noises.
## PCB
![](https://github.com/mustafasenel/CC-CV_Adjustable_Buck_Converter/blob/main/PCB_print_color.jpg?raw=true)

Resources/Kaynaklar

https://www.pcbway.com/blog/technology/0_30V__0_7A_Adjustable_Switching_Power_Supply.html
http://www.xlsemi.com/datasheet/xl4016%20datasheet.pdf
