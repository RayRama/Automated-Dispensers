# Automated Dispensers With Ultrasonic Sensor
Dispenser otomatis dengan sensor jarak atau ultrasonik merupakan jenis dispenser yang menggunakan teknologi sensor untuk mengdeteksi keberadaan tangan atau objek di depannya. Alat ini akan secara otomatis mengeluarkan cairan, seperti air minum atau sabun, ketika sensor mendeteksi adanya tangan atau objek di depannya. Dispenser otomatis dengan sensor jarak atau ultrasonik sangat berguna untuk menjaga kebersihan tangan dan menghindari kontak langsung dengan cairan yang dikeluarkan. Selain itu, alat ini juga dapat membantu menghemat cairan dengan mengeluarkannya hanya ketika diperlukan.

# Our Team
![Teams](https://img.shields.io/badge/Our%20Team-Team%203-blue)
<div align='center'>

<br>

[![1217050117](https://img.shields.io/badge/117-Ray%20Ramadita-blue)](https://github.com/RayRama) 
  [![1217050133](https://img.shields.io/badge/133-Silvia%20Nurrobianti-blue)](https://github.com/) [![1217050131](https://img.shields.io/badge/131-Sami%20Irhamnillah-blue)](https://github.com/) [![1217050146](https://img.shields.io/badge/146-Yuda%20Ristian%20A-blue)](https://github.com/) [![1217050140](https://img.shields.io/badge/140-Wiki%20Nurrohman-blue)](https://github.com/) [![1217050117](https://img.shields.io/badge/100-Muhammad%20Nuzul%20Rizka-blue)](https://github.com/)
  <br> [Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

</div>

## Alat dan Bahan
1. Kardus
2. Lem tembak/lem bakar
3. Alat lem tembak
4. Penggaris
5. Kater
6. Gunting
7. Balpoin/pensil
8. Sensor Ultrasonic
9. Relay 5V
10. Selang Pompa 1 m
11. Mini Pompa 3V (DC)
12. Casing Akrilik Arduino (Opsional)
13. Kabel Jumper Male to Female 20 cm
14. Arduino Uno
15. Kabel Data Tipe C
16. Kabel Data Printer (Tipe B)
17. Adaptop Charger HP

## Flowchart 
Berikut adalah flowchart project ini
<br>![Flowchart_assets](assets/flowchart.jpg)

## Source Code
Untuk menjalankan kodenya, anda harus menginstall Arduino IDE terlebih dahulu yang bisa didownload melalui link berikut (https://www.arduino.cc/en/software)
```ino
#define trigger 5
#define echo 4
#define Relay 3
float time=0,distance=0;
void setup()
{
  Serial.begin(9600);

 pinMode(trigger,OUTPUT);
 pinMode(echo,INPUT);
 pinMode(Relay,OUTPUT);

 delay(2000);
}

void loop()
{
 measure_distance();

 if(distance>5)
 {
   digitalWrite(Relay,HIGH);
 }
 else
 {
   digitalWrite(Relay,LOW);
 }

 delay(300);
}

void measure_distance()
{
 digitalWrite(trigger,LOW);
 delayMicroseconds(2);
 digitalWrite(trigger,HIGH);
 delayMicroseconds(10);
 digitalWrite(trigger,LOW);
 delayMicroseconds(2);
 time=pulseIn(echo,HIGH);

 distance=time*200/20000;
}
```
## Langkah - Langkah Pembuatan
1. Pola kardus menggunakan penggaris dan pensil/balpoin menjadi persegi panjang untuk kerangka penyimpana alat-alat yang digunakan dan penyimpanan air.
2. Lem kardus yang sudah memiliki pola, lalu diamkan hingga lem benar-benar merekat dan kardus terbentuk menjadi apa yang telah dipola.
3. Pola kembali 1 lembar kardus untuk menutup bagian bawah pada dispenser agar kardus yang sudah terbentuk bisa berdiri dan membuat alas untuk gelas nantiya.
4. Setelah pola terbentuk rekatkan dengan kardus yang persegi Panjang.
5. Buat kembali pola untuk penutup bagian atas dispenser dan bagian depan dispenser untuk menutupi bagian selang air yang nantinya akan digunakan.
6. Apabila pola sudah terbentuk rekatkan kembali dengan pola yang sudah terbentuk sebelumnya.
7. Kasih 2 lubang sebesar sensor dibagian depan dispenser yang setara dengan gelas yang akan digunakan.
8. Tempelkan sensor pada lubang yang telah dibuat menggunakan lem tembak/lem bakar.
9. Buat dudukan untuk Arduino dibagian dalam kardus yang berbentuk persegi Panjang agar Arduino dapat terlindungi.
10. Tempelkan kerangka dudukan untuk Arduino yang telah terbentuk pada bagian dalem samping dispenser.
11. Setelah semua terpasang lalu instalkan semua komponen menggunakan kabel.
12. Lalu apabila sudah terpasang semua dispenser otomatis telah jadi dan siap untuk digunakan.

## Lainnya
Untuk lebih lanjut, anda bisa membaca artikel berikut [Automated Dispensers With Ultrasonic Sensor](https://medium.com/@silvianurrobianti/automated-dispensers-with-ultrasonic-sensor-7eb52714f260)
