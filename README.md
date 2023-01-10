# 2.4-GHz-ISM-antennas
Benchmark test of widely available 2.4 GHz ISM band antennas

Heinrich Diesinger,
Univ Lille, Univ Polytech Hauts France, CNRS, Centrale Lille, Junia, Inst Elect Microelect & Nanotchnol (IEMN) UMR 8520, F-59652 Villeneuve d'Ascq, France

The objective of this study is the comparison of a number of antennas for the 2.4 GHz ISM band, suitable for WiFi, Bluetooth, BLE, LoRa 2.4 GHz, QO-100 Satcom, FPV, that are either commercially available or can be built with moderate effort. The primary issues are the safe matching of the antenna to a transceiver, accuracy of the vendor specifications, and performance comparison between commercial antennas and their DIY competitors.

![alu_yagi_ali](https://user-images.githubusercontent.com/96028811/211599075-faf3062d-2074-4fc8-a724-48743adc599f.jpg)
![image](https://user-images.githubusercontent.com/96028811/211596007-e4ca0854-893d-4faa-b1d1-66a5413ddd26.png)
![image](https://user-images.githubusercontent.com/96028811/211596030-f09eaba9-495f-4006-805a-5ed0fcf44026.png)
![image](https://user-images.githubusercontent.com/96028811/211596043-acffcc64-0a89-4919-af14-53300d6922c6.png)
![image](https://user-images.githubusercontent.com/96028811/211596064-15596a13-a679-4fc5-954a-a28741875552.png)



The first part is a description of each antenna along with a VSWR measurement on the Nano-VNA to check matching with the transceiver; the second part is a comparative test of directivity/gain. The candidates are :

- Short rubber antenna lambda/4, nominal 2 dBi

- Longer rubber antenna, nominal 5 dBi

- Patch antenna QO-100 « Poty »: LHCP feeder for parabolic dish

- Modified QO-100 patch antenna with 22 mm washers instead of tube

- RHCP patch antenna downsized from Inmarsat antenna

- Yagi 17 element 50 cm, alu: advertised gain 16..18 dBi, by some vendors 25 dBi

- PCB printed Yagi antenna: gain advertised up to 10.5 dBi

- Patch quad array, linear polarisation: gain advertised 14 dBi

- Cantenna 83 mm diameter, 250 g coffee can

- Cantenna 97 mm diameter, 500 g coffee can




I. Description of antennas and VSWR measurements


1. Short rubber antenna 2 dBi

![image](https://user-images.githubusercontent.com/96028811/211601575-3d80e10f-f113-4694-a5c5-3fd16739b211.png) ![image](https://user-images.githubusercontent.com/96028811/211601603-5316723f-70de-4f82-a260-5ef66a0374db.png)

The yellow trace shows the return loss S11 in dB. The VSWR (blue trace) shown here is 1.43 @ 2460 MHz; it is very close to unity in the specified range. Note: the phase of the Smith chart (green) is not correct because the VNA is still calibrated for including the 20 cm cable but the antenna is in this case mounted directly to the VNA without the piece of cable.
The low VSWR is not surprising since these antennas are known to suffer from dissipation, treading gain against good matching.


2. Long rubber antenna 5 dBi

![image](https://user-images.githubusercontent.com/96028811/211602781-2590abba-77c7-4011-a079-aea7ff94a512.png)   ![image](https://user-images.githubusercontent.com/96028811/211602821-1427bc84-c09e-4a17-80f4-4f8d12a800c0.png)

The VSWR minimum is @ 2320 MHz. At 2460 MHz it is 2.92, not good for this kind of antenna that is expected, as its shorter counterpart, to give a perfect match rather than a high gain. It was actually sold as a 433 MHz antenna but there is no VSWR minimum near this frequency either, so we consider it as a typical 5 dBi WiFi antenna. The frequency deviation cannot be attributed to using it with the wrong counterpoise because at this range of frequency it is negligible. The counterpoise is most important in VHF only but not here. A second VSWR dip appears around 2650 MHz : The measurement resolution seems to be insufficient for resolving it because the Smith chart (green) has jumps between 3 measurement points visible as straight lines.


3. Patch QO-100, metal plates soldered on waveguide tube

This is the original QO-100 satellite dish feeder for QO-100 uplink at 2.4 GHz, from
http://www.hybridpretender.nl/patch.pdf
http://docplayer.net/166276448-Es-hail-2-oscar-100-dual-band-patch-antenna.html
In summary, it is taken from a ham radio project that consists of converting a parabolic dish antenna into a dual band 2.4 GHz/10.7 GHz antenna for up- and downlink to a geostationary satellite that accommodates (among others) a ham radio transverter.

![image](https://user-images.githubusercontent.com/96028811/211603867-f7e71a43-8fa2-4c64-9148-44547f9ebc94.png)   ![image](https://user-images.githubusercontent.com/96028811/211603886-6bed839e-2413-41a3-9879-d3bd3d82d654.png)

Left : QO-100 patch feeder being assembled by soldering two brass plates on a copper plumbing tube ;  right : QO-100 feeder mounted to a parabolic offset dish, along with a LNB for the 10.7 GHz downlink.

![image](https://user-images.githubusercontent.com/96028811/211603947-cebf4d7f-88b6-4930-b740-de09b6f12761.png)   ![image](https://user-images.githubusercontent.com/96028811/211603992-51a76ab9-b3a2-4742-b2a3-0ac0611035a4.png)

VSWR: 1.9 @ 2400 MHz, 2.77 @ 2500 MHz; minimum 1.44 @ 2360 MHz

The VSWR minimum is slightly below the target frequency of 2450 MHz. Once soldered, it is difficult to trim and fine tune.


4. Patch with same dimensions as QO-100, using 22 mm washers instead of the tube

For our purpose the waveguide tube for passing the QO-100 satellite downlink at 10.7 GHz to the LNB is not needed. In a successive version, an electrically identical patch antenna was therefore built by replacing the tube by 22 mm washers, eliminating the critical solder step.

![image](https://user-images.githubusercontent.com/96028811/211604264-e0081365-2e93-41e2-bd83-6769fc303ed4.png)   ![image](https://user-images.githubusercontent.com/96028811/211604298-37855168-7b76-4ce0-a9cf-3deded105b44.png)

Left : LHCP feeder patch antenna on Nano-VNA ; right : suction cup window version

![image](https://user-images.githubusercontent.com/96028811/211604362-cf9e0b6d-3815-4287-8d9a-52bcc1f455c3.png)

VSWR: 2.47 @ 2400 MHz; 3.25 @ 2500 MHz, minimum 2.3 @ 2380 MHz

Note that because the antenna is screw mounted instead of soldered, the back plate can be made from aluminum; the radiator still is brass because the center pin of the sma connector is soldered to it.


5. Patch custom made, downsized from Inmarsat/GPS/Iridium: 

Next, an antenna that is not for QO-100 and does not feature the wavegide tube was then made by downscaling to 2450 MHz a L-band Inmarsat antenna, proposed by ham operator Adam 9A4QAV,: https://www.rtl-sdr.com/building-and-testing-an-l-band-patch-antenna-for-inmarsat-c-reception/

https://www.rtl-sdr.com/building-and-testing-an-l-band-patch-antenna-for-inmarsat-c-reception/
for 1500 MHz:
Reflector Size: 170 mm x 170 mm
Patch Size: 98 mm x 98 mm
Corner Trim: 21 mm from top right and bottom left corners
Coax Connection (Probe): 25 mm from bottom edge
Height of patch from reflector: 7 mm

downscaled 1500 MHz  → 2450 MHz
Reflector Size: 104 mm x 104 mm
Patch Size: 60 mm x 60 mm
Corner Trim: 12.8 mm (approx 13 mm) from top right and bottom left corners
Height of patch from reflector: 4.29 mm

trimmed until it works:
Reflector Size: 104 mm x 104 mm
Patch Size: 58 mm x 58 mm
Corner Trim: 13 mm from top right and bottom left corners
Coax Connection (Probe): 23 mm from left, 8 mm from top (this assymmetric arrangement was inspired from  QO-100 antenna)
Height of patch from reflector: 4 mm

![image](https://user-images.githubusercontent.com/96028811/211604552-9587b174-2aab-4357-9f8f-c343fa2b000a.png)   ![image](https://user-images.githubusercontent.com/96028811/211604591-b969dc99-4fc2-44e4-acb4-a2da68c75cda.png)

Result: VSWR of 3.08 @ 2440 MHz, up to 3.77 within 2400 .. 2500 MHz

 The downscaled version is smaller than the version with the tube or 22 mm washer as can be expected. It suggests that if the frequency should be too low, it can be raised by inserting a larger diameter screw or washers in the center.

By the way in the video, Adam says that the center contact is an arbitrary choice to make it DC grounded and protect the LNA input against ESD. The center is a zero impedance spot and for the antenna it is indifferent whether grounded or isolated.

Note that the Inmarsat antenna is RHCP and the feeder for QO-100 is LHCP because the polarisation is flipped by the parabolic dish to RHCP. RHCP is the standard for satcom.


6. Yagi 50 cm, aluminum, 17 elements, advertised gain 16..18 dBi, by some vendors 25 dBi

![image](https://user-images.githubusercontent.com/96028811/211604940-ce83df23-9b00-4257-8121-2b5f866da554.png)   ![image](https://user-images.githubusercontent.com/96028811/211604973-d998f3a9-33b6-4a3e-a4c4-9337208036b5.png)

The antenna requires extensive repair work before putting into service, exactly as described at https://hackaday.io/project/158995/logs?sort=oldest

It seems that the antenna is commercialized since >3 years with a frequently lacking connection between the cable and the driven element. For the antenna to work it is of paramount interest that the feed line is connected to the active element.

Other observations are the equidistant elements of same length, whereas a usual Yagi antenna has different length elements that are not equidistant. In general, the impedance decreases with increasing number of elements, hence a folded dipole with its 300 Ohm is possibly reduced to 50 Ohm with 15 directors. (open dipole: 75 Ohm).

![image](https://user-images.githubusercontent.com/96028811/211605094-b87b78ec-a97f-46bc-81df-611f2f5ded6b.png)   ![image](https://user-images.githubusercontent.com/96028811/211605129-97a7a2f8-cee1-4ce4-bc32-b985a17b3676.png)

Result: VSWR varies between 1.31 and 1.83, over a range >> 2.4..2.5 GHz; measurement includes the non-detachable cable, 142 cm RG-58. Erratum: previoulsy cable length wrongly given as 60 cm.

Curiosity:
Relation between number of oscillations and cable length: for every wavelength that fits on twice the cable length (back and forth), we get one oscillation of S11 or the VSWR or one turn around the Smith chart:
cn/f = lambda; n is the velocity factor 0.666 of the coax; Z is the number of S11 oscilations

2L(f2-f1)/(cn) = Z = 15;    L = Zcn/(2 (f2-f1)) = 1.5m, determined from number of oscillations

Also note that 1.5 m of RG-58 cable with loss 40 dB/100 ft reduces a feedpoint VSWR of 3 to 1.93


7. Yagi 50 cm, alu,  unmodified as from factory

A second unit of these antennas recently arrived and it turned out that this time the cable is not disconnected because it presents a DC short. It was then characterized as is, to find out whether the piece of mini coax that is believed to act as a stub, would improve the performance beyond the antenna that underwent repair work, sacrifying the stub.

However, it seems that it rather deteriorates the behavior:

![image](https://user-images.githubusercontent.com/96028811/211605429-241191f6-6f4b-42e0-b2b4-5b6ab6e7f381.png)   ![image](https://user-images.githubusercontent.com/96028811/211605460-254f7b7d-1981-496a-bc2d-0869cae00b53.png)

VSWR: 1.68 @ 2450 MHz, 5.2 @ 2480 MHz. The fluctuations of VSWR within the desired frequency range are larger for the unmodified factory configuration containing the 5 cm piece of coax acting as a stub.

Note : during the measurement, the antenna was not laying on the floor ; on the photograph the acquisition is halted and the screen shows the data acquired in free space.


8. Yagi printed: gain advertised up to 10.5 dBi

![image](https://user-images.githubusercontent.com/96028811/211605590-1cbfd948-294b-4c02-bb36-31da629cc6fa.png)   ![image](https://user-images.githubusercontent.com/96028811/211605611-f327250d-7b00-4b61-8e1b-38d76b20d676.png)

Result: 

![image](https://user-images.githubusercontent.com/96028811/211605682-15adc74a-715b-45fc-8146-e755724940df.png)   ![image](https://user-images.githubusercontent.com/96028811/211605707-53677188-8a45-4ae2-b2c4-3aaeafc53888.png)

The VSWR has its minimum exactly in the middle of the desired frequency range and is low enough to assure an almost perfect match :
1.18 @ 2450, 1.49 @ 2400, nicely centered around 2450 MHz and useable over a 100 MHz width.


9. Quad patch array 2 x 2:  gain advertised 14 dBi

![image](https://user-images.githubusercontent.com/96028811/211605845-e16f824c-7070-4b1a-98cf-d41d43acffd9.png)   ![image](https://user-images.githubusercontent.com/96028811/211605899-9b5491d5-2255-4d38-b0fd-ba39d1a24a9a.png)

The antenna contains a PCboard consisting of the 4 patches and a feeder network. Apparently it did or still does exist a version made from sheet metal and without PCboard wich is possibly even more performant since it avoids distortion of the field by the dielectric at the edges of the patches. Also note that many WiFi routers contain internal patch antennas.

Result:

![image](https://user-images.githubusercontent.com/96028811/211605965-6cb2c3a7-544f-438c-ad1e-a39f7bd6fb7c.png)   ![image](https://user-images.githubusercontent.com/96028811/211605988-e48e7510-035e-4c94-98b5-9445453335e6.png)

VSWR 1.03 @ 2400 MHz,  4.6 @ 2480; the dip is not centered at 2450 MHz and very sharp.

Note: before disassembly and reassembly, the VSWR dip was less pronounced (right image). Cured by curiosity ? Apparently the cable was longer while recording the left (additional 20 cm coax?).
This antenna is expected to give the best results at the lower end of our desired frequency range.

![image](https://user-images.githubusercontent.com/96028811/211606054-f21b3589-dc8c-4191-bba5-bf22fe09eab1.png)

Sheet metal version, Ideaworks USB WIFI Antenna : https://www.youtube.com/watch?v=LMalVB1fu2g


10. Cantenna 83 mm diameter

250 g coffee can, dimensions : 83 mm diameter, 145 mm height

![image](https://user-images.githubusercontent.com/96028811/211606251-7579eb21-7acd-4acb-bfba-898bc17ef6c1.png)   ![image](https://user-images.githubusercontent.com/96028811/211606283-3d596869-a933-4cff-9459-ae12a69ed43b.png)

Result:

![image](https://user-images.githubusercontent.com/96028811/211606342-a8c31f7f-0e1b-4d05-a81f-aac041db69fb.png)   ![image](https://user-images.githubusercontent.com/96028811/211606373-bb08e5fe-2c9b-49c9-89ad-36a535b86638.png)

VSWR dip unchangeably centered at 2530 MHz : 2.0 @ 2530, 3.48 @ 2400, 2.30 @ 2500; increasing the radiator length from 31 mm to 34 mm does not lower the optimum frequency below 2530 MHz; probably the can is too small.

A website :
http://f8kgb.chez-alice.fr/presentation_antenneeh_dipoleetvinverse_antennewifi.htm
gives a length as function of diameter. In contrast to what is stated, it is not the can length, but the wavelength for the TEM_00 mode that becomes longer as the can diameter shrinks, because part of the k vector is consumed for fitting the mode into the can. Here for 83 mm diameter, the dipole is placed lambda/4 = 66 mm in front of the bottom (= reflector). This appears (unreasonably?) long compared to the freespace quarter wavelength.


11. Cantenna 97 mm diameter

Cantenna from 500 g coffee can, dimensions : 97 mm diameter, 185 mm height;
for diameter 97 mm, the above  website yields lambda/4 = 45.5 mm for the position of radiator from bottom; the radiator length was shortened until SWR was optimized at 2450 and we find exactly 31 mm;

![image](https://user-images.githubusercontent.com/96028811/211606498-4d06d758-59b7-44e4-8071-42c264009810.png)   ![image](https://user-images.githubusercontent.com/96028811/211606534-3ed8568f-5fd6-4513-a19a-c12a3fc4a2c6.png)

Result :
VSWR: 1.05 @ 2450 MHz, < 1.1 over the entire range 2400 .. 2500 MHz ;
Note that a second VSWR minimum appears at 2620 MHz. This might be the appearance of the next higher mode above TEM00.




II. Relative gain/directivity test for comparing the antennas to each other

The relative gain of the antennas shall now be compared. To do so, a test transmitter with a SX1281 transceiver module and a printed 5 element Yagi is set to emit in CW mode.

![image](https://user-images.githubusercontent.com/96028811/211606670-06e2912a-be1c-4f01-9863-3bf1a2c29112.png)

Setup for the field test: antenna gain measurement

Conditions: transmitted power 5 dBm, in CW mode, 2410 MHz, 4 meter distance between transmitting and receiving antenna, transmitter aiming into space, RSSI measured by a power meter with -52 dBm sensitivity

Then, the antennas to be tested are made to face the test transmitter from 4 meters distance, and the incoming signal is measured by a RF power meter. Lacking an anechoic chamber, the transmitter is aiming into the sky/space to avoid reflections and multipath propagation. This leads to RSSI values on the power meter typically of -30 .. -20 dBm, far above the sensitivity of -52 dBm and any unintentional receptions of nearby ISM band devices. Note that the frequency value entered into the power meter seems to be a calibration factor and it does not provide filtering.

![image](https://user-images.githubusercontent.com/96028811/211606741-7463f1da-5b85-4306-9145-959f725931b5.png)   ![image](https://user-images.githubusercontent.com/96028811/211606795-4bfb0522-0fe5-4b15-bf95-40940f07b157.png)

Also note that here the Yagi antenna has been modified according to Hackaday and furthermore features a SMA connector near the feedpoint instead of the permanently attached cable, allowing VSWR and gain measurements closer to its feedpoint. The quad patch antenna was modified similarly with a SMA connector.

![image](https://user-images.githubusercontent.com/96028811/211606860-1b873b54-6c1a-49fd-a684-ba4f3968ff1a.png)

The test transmitter, 5 dBm aiming at the sky to avoid multipath propagation / reflections. Two printed Yagi antennas were available allowing to keep one as transmitter and use another as DUT.


The antennas were then aimed at the transmitter on the stretched out arm aiming downwards. The linear antennas showed that the emitted polarization was perfectly linear. By rotating e.g. the rubber antenna horizontally, the signal strength dropped below the detection threshold.

The homemade patch antennas that are supposed to have circular polarization were tested in V and H polarization, V meaning that the feedpoint is up or down, and H that it is to the side. Because it had been heard that the polarization is not always perfectly circular. Indeed, most times the V polarization is the preferential one, however only 2 specimen had almost identical values for V and H, showing that it is probably well circularly polarized. This shows that the circular polarization is difficult to achieve and depends critically on the dimensions.

Antennas that are marked (a), (b), (c) are available as several specimen.



The results : raw signal strengths
 
Received power :

Antenna						RSSI “V“		RSSI “H“

Short rubber, nominal gain 2 dBi: 			-36.9 dBm		-52 dBm (noise)
Patch QO-100 Poty: 					-25.8 dBm		-30.4 dBm
Patch QO-100 with 22 mm washers  (a) 		-36.4 dBm		-34.8 dBm
Patch QO-100 with 22 mm washers  (b)		-28.1 dBm		-28.3 dBm
Patch RHCP downsized from Inmarsat (a)		-28.6 dBm		-28.3 dBm
Patch RHCP downsized from Inmarsat (b)		-28.6 dBm		-31.4 dBm
Patch RHCP downsized from Inmarsat (c)		-27.7 dBm		-31.0 dBm
Yagi 50 cm, alu: advertised gain 16..18 dBi 		-23.7 dBm
Yagi printed: nominal gain up to 10.5 dBi 		-25.5 dBm
Quad patch array: nominal gain 14 dBi		-21.7 dBm
Cantenna 83 mm:					-28.1 dBm
Cantenna 97 mm: 					-24.6 dBm




