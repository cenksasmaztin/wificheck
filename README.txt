#wificheck



#Copyright (c) 2024  Cenk Sasmaztin <cenk@oxoonetworks.com>
#All rights reserved.

#Redistribution and use in source and binary forms, with or without
#modification, are permitted provided that the following conditions
#are met:
#1. Redistributions of source code must retain the above copyright
#notice, this list of conditions and the following disclaimer.
#2. Redistributions in binary form must reproduce the above copyright
#notice, this list of conditions and the following disclaimer in the
#documentation and/or other materials provided with the distribution.

#THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS'' AND
#ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
#IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
#ARE DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE
#FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
#DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
#OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
#HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
#LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
#OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
#SUCH DAMAGE.






#PURPOSE of this SCRIPT

Overview

This Python script is designed to monitor and analyze the performance of Wi-Fi networks in real-time. It collects various metrics, such as signal strength, SNR (Signal-to-Noise Ratio), data rates, throughput, and network performance indicators like ping times, DHCP, DNS, and authentication status. The tool displays results in a tabular format on the terminal and generates a summary report with a graphical visualization saved as a PDF.
This code must be running Rasberr pi devices.This device connect costumers corparete wifi networks.

Features

	•	Real-Time Monitoring: Continuously collects and displays Wi-Fi performance data.
	•	Network Performance Metrics: Measures signal strength, SNR, data rates, throughput, and latency (gateway and internet ping).
	•	Connectivity Tests: Performs DHCP and DNS checks to ensure network functionality.
	•	Authentication Method Detection: Identifies the Wi-Fi authentication protocol in use (e.g., WPA3, WPA2).
	•	Automatic Reporting: Generates and saves a summary report with graphical analysis at the end of the monitoring session.
	•	Customizable: Default network interface and other parameters can be adjusted for specific needs.

Installation

Ensure you have the required Python packages installed:
pip install matplotlib reportlab

Usage

Run the script using Python 3:

sudo python3 wificheck301024.py

During Execution

	•	The script displays a real-time table of Wi-Fi performance metrics.
	•	To stop the analysis, press CTRL+C.

After Execution

	•	A summary report is displayed in the terminal.
	•	A detailed PDF report with graphical analysis is saved in the report/ directory.

Requirements

	•	Python 3.x
	•	matplotlib for graph generation
	•	reportlab for PDF report creation
	•	wpa_cli for Wi-Fi status commands
	•	iw for Wi-Fi information gathering
	•	ping utility for latency checks
	•	Network interface wlan0 (modifiable in the code)

Report Details

	•	Summary: Includes average signal strength, SNR, data rate, throughput, ping times, and the number of successful, poor, and failed tests.
	•	Graphical Visualization: Line graphs showing variations in signal strength, SNR, and ping times over the monitoring period.

Customization

	•	Modify the interface variable in the auth_check and get_wifi_info functions to use a different network interface.
	•	Change ping targets in gateway_check and internet_check for different network environments.

Author

Created by Oxoo Networks LLC.

Example print

Timestamp  
MAC Address
SSID
AP
Frequency
Channel
Signal Strengt
Data Rate
Throughput
SNR
GTW Ping
INT Ping
DHCP
DNS
Auth
WIFI Performance

#TR

#BU SCRIPTİN AMACI

Genel Bakış

Bu Python scripti, Wi-Fi ağlarının performansını gerçek zamanlı olarak izlemek ve analiz etmek üzere tasarlanmıştır. Sinyal gücü, SNR (Sinyal-Gürültü Oranı), veri hızları, throughput gibi çeşitli ölçümleri ve ağ performansı göstergeleri (ping süreleri, DHCP, DNS ve kimlik doğrulama durumu) toplar. Araç, sonuçları terminalde tablo biçiminde gösterir ve grafiksel bir görselleştirme ile özet rapor hazırlar ve PDF olarak kaydeder. Bu kodun Raspberry Pi cihazlarında çalıştırılması ve bu cihazın müşterilerin kurumsal Wi-Fi ağlarına bağlanması gerekmektedir.

Özellikler

Gerçek Zamanlı İzleme: Wi-Fi performans verilerini sürekli olarak toplar ve görüntüler.
Ağ Performansı Ölçümleri: Sinyal gücü, SNR, veri hızları, throughput ve gecikme (gateway ve internet ping) ölçümleri yapar.
Bağlantı Testleri: Ağ işlevselliğini sağlamak için DHCP ve DNS kontrolleri yapar.
Kimlik Doğrulama Yöntemi Tespiti: Kullanılan Wi-Fi kimlik doğrulama protokolünü (ör. WPA3, WPA2) belirler.
Otomatik Raporlama: İzleme oturumunun sonunda grafiksel analiz içeren özet bir rapor oluşturur ve kaydeder.
Özelleştirilebilir: Varsayılan ağ arayüzü ve diğer parametreler özel ihtiyaçlara göre ayarlanabilir.
Kurulum

Gerekli Python paketlerinin kurulu olduğundan emin olun:

pip install matplotlib reportlab
Kullanım

Scripti Python 3 ile çalıştırın:

sudo python3 wificheck301024.py
Çalıştırma Sırasında

Script, Wi-Fi performans ölçümlerinin gerçek zamanlı bir tablosunu görüntüler.
Analizi durdurmak için CTRL+C tuşlarına basın.
Çalıştırma Sonrası

Terminalde bir özet rapor görüntülenir.
Grafiksel analiz içeren ayrıntılı bir PDF raporu report/ dizinine kaydedilir.
Gereksinimler

Python 3.x
Grafik oluşturmak için matplotlib
PDF raporu oluşturmak için reportlab
Wi-Fi durumu komutları için wpa_cli
Wi-Fi bilgisi toplamak için iw
Gecikme kontrolleri için ping aracı
Ağ arayüzü wlan0 (koddaki ayarlanabilir)
Rapor Detayları

Özet: Ortalama sinyal gücü, SNR, veri hızı, throughput, ping süreleri ve başarılı, zayıf ve başarısız test sayıları içerir.
Grafiksel Görselleştirme: İzleme süresi boyunca sinyal gücü, SNR ve ping sürelerindeki değişimleri gösteren çizgi grafikleri.
Özelleştirme

auth_check ve get_wifi_info işlevlerindeki interface değişkenini değiştirerek farklı bir ağ arayüzü kullanabilirsiniz.
gateway_check ve internet_check işlevlerindeki ping hedeflerini farklı ağ ortamları için değiştirebilirsiniz.
Yazar

Oxoo Networks LLC tarafından oluşturulmuştur.

Örnek Çıktı

Zaman Damgası
MAC Adresi
SSID
AP
Frekans
Kanal
Sinyal Gücü
Veri Hızı
Throughput
SNR
GTW Ping
INT Ping
DHCP
DNS
Kimlik Doğrulama
WiFi Performansı
