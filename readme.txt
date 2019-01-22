Lojik Devre Benzetimi

Fatma Deðirmenci  -	170201008
Berfin Kösemen	  -	170201058

Bu readme.txt dosyasý, Lojik Devre Benzetimi projesine aittir.
Bu paket, kaynak kodu ile ayný dizin içerisinde bulunacaktýr.


1-PAKETÝN ÝÇERÝÐÝ:
-------------------
kaynak.zip - Projenin kaynak kodunun ve yardýmcý dosyalarýn ziplenmiþ hali.
170201008-170201058.txt - Projenin tek dosyaya indirgenmiþ salt kaynak kodu.
rapor.doc - Proje raporu.
readme.txt - Bu dosya.
-------------------


2-SÝSTEM GEREKSÝNÝMLERÝ:
-------------------
gcc - GNU Compiler Colection - http://gcc.gnu.org/
-------------------


3-KURULUM:
-------------------
Paket içeriðini yukarýda görebilirsiniz.

Bu kod, iki adet Windows kurulu makinede çalýþtýrýldý:
- Fatma'nýn Windows 10 yüklü dizüstü bilgisayarýnda.
- Berfin'in Windows 10 yüklü masaüstü bilgisayarýnda.

Bu iki durumda da kod, herhangi bir hata vermeden, daha önceden belirlenen kriterlere
uygun çalýþtý.

Windows harici bir makinede çalýþtýrmak istiyorsanýz, kaynak kodu Windows
baðýmlýlýklarýndan ayýrýp derlemeniz gerekiyor.

-------------------


4-KODU DERLEMEK:
------------------
Artýk bilgisayarýmýzda kurulu olan GCC ile kodu kolayca derleyebiliriz.

Windows için:

>gcc 170201008-170201058.cpp –o 170201008-170201058.exe

Linux / Unix için:

>gcc 170201008-170201008.cpp -o 170201008-170201058


Derleme bittikten sonra kolayca programý çalýþtýrabilirsiniz.
------------------


5- PARAMETRELER
-------------------
////Kodun çalýþmasý için baþlangýçta herhangi bir parametre gerekmiyor.

Kodun çalýþmasý için baþlangýçta "devre.txt" ve "deger.txt" dosyalarýnýn
kaynak kodun olduðu dizin/klasörde bulunmasý gerekmektedir.
------------------


6- PROGRAMIN KULLANIMI
-----------------------------
Lojik Devre Benzetimi, "devre.txt" dosyasýndan mantýksal bir devreyi 
ve "deger.txt" dosyasýndan giriþ ve çýkýþlarýn deðerlerini okuyarak, 
kullanýcýnýn girdiði komutlara göre, kapý yayýlým gecikmeleri de 
dikkate alýnarak devreyi simule eder.

Program ilk çalýþtýrýldýðýnda "devre.txt" içindeki satýrlarý yorumlayýp
komut çalýþtýrabilir hale gelir.

Kullanýcýnýn komut girmesi gerektiðini bildirmek amacý ile ekrana 
prompt(uyarý) karakteri '>' yazdýrýlýr. Kullanýcý herhangi bir komut 
girdikten sonra gereken iþlemler yapýlýnca -sonlandýrma komutu olan 
C/c komutu girilmediði sürece- tekrar prompt(uyarý) karakteri '>' ekrana 
yazdýrýlýr.

Komutlar büyük veya küüçük harf olabilir (not case-sensitive).

Devre yükleme (Y/y) ve ilklendirme(I/i) komutu girilmeden diðer komutlar
(H/h, L/l, S/s, G/g, G*/g*, K/k, C/c) aktifleþmemektedir. Öncelikle Y ve I
komutlarýnýn girilmesi gereklidir.

Var olan komutlar dýþýnda farklý bir komut girilmeye çalýþýldýðýnda hata
mesajý ekrana yazdýrýlýr ve kullanýcýdan tekrar komut girilmesi beklenir.

Kullanýcýnýn girdiði her komut, komut.txt dosyasýna yazdýrýlýr. Tüm yapýlan
iþlemler ise tarih/saat kaydedilerek log.txt dosyasýna yazdýrýlýr.

C/c komutu girildiðinde program sonlandýrýlýr.

Komutlar 			   ve 		Ýcralarý
Y <devre.txt> 					“devre.txt” dosyasýndan devreyi yükler
I 						“deger.txt” icindeki degerlerle devre ilklendirilir
H <giris ucundan biri/birileri> 		Ilgili uç/uçlarý Lojik-1 yapar
L <giris ucundan biri/birileri> 		Ilgili uç/uçlarý Lojik-0 yapar
S 						Devreyi simüle eder
G <giris/çýkýs ucundan biri/birileri> 		Ilgili uç/uçlarýn seviyesini (0 veya 1) konsolda gösterir
G* 						Tüm uçlarýn seviyesini (0 veya 1) konsolda gösterir
K <komut.txt> 					“komut.txt” dosyasý içindeki komutlarý konsoldan oldugu gibi icra eder
C 						 Benzetimden çýkýs yapar
