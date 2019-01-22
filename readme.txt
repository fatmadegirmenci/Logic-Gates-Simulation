Lojik Devre Benzetimi

Fatma De�irmenci  -	170201008
Berfin K�semen	  -	170201058

Bu readme.txt dosyas�, Lojik Devre Benzetimi projesine aittir.
Bu paket, kaynak kodu ile ayn� dizin i�erisinde bulunacakt�r.


1-PAKET�N ��ER���:
-------------------
kaynak.zip - Projenin kaynak kodunun ve yard�mc� dosyalar�n ziplenmi� hali.
170201008-170201058.txt - Projenin tek dosyaya indirgenmi� salt kaynak kodu.
rapor.doc - Proje raporu.
readme.txt - Bu dosya.
-------------------


2-S�STEM GEREKS�N�MLER�:
-------------------
gcc - GNU Compiler Colection - http://gcc.gnu.org/
-------------------


3-KURULUM:
-------------------
Paket i�eri�ini yukar�da g�rebilirsiniz.

Bu kod, iki adet Windows kurulu makinede �al��t�r�ld�:
- Fatma'n�n Windows 10 y�kl� diz�st� bilgisayar�nda.
- Berfin'in Windows 10 y�kl� masa�st� bilgisayar�nda.

Bu iki durumda da kod, herhangi bir hata vermeden, daha �nceden belirlenen kriterlere
uygun �al��t�.

Windows harici bir makinede �al��t�rmak istiyorsan�z, kaynak kodu Windows
ba��ml�l�klar�ndan ay�r�p derlemeniz gerekiyor.

-------------------


4-KODU DERLEMEK:
------------------
Art�k bilgisayar�m�zda kurulu olan GCC ile kodu kolayca derleyebiliriz.

Windows i�in:

>gcc 170201008-170201058.cpp �o 170201008-170201058.exe

Linux / Unix i�in:

>gcc 170201008-170201008.cpp -o 170201008-170201058


Derleme bittikten sonra kolayca program� �al��t�rabilirsiniz.
------------------


5- PARAMETRELER
-------------------
////Kodun �al��mas� i�in ba�lang��ta herhangi bir parametre gerekmiyor.

Kodun �al��mas� i�in ba�lang��ta "devre.txt" ve "deger.txt" dosyalar�n�n
kaynak kodun oldu�u dizin/klas�rde bulunmas� gerekmektedir.
------------------


6- PROGRAMIN KULLANIMI
-----------------------------
Lojik Devre Benzetimi, "devre.txt" dosyas�ndan mant�ksal bir devreyi 
ve "deger.txt" dosyas�ndan giri� ve ��k��lar�n de�erlerini okuyarak, 
kullan�c�n�n girdi�i komutlara g�re, kap� yay�l�m gecikmeleri de 
dikkate al�narak devreyi simule eder.

Program ilk �al��t�r�ld���nda "devre.txt" i�indeki sat�rlar� yorumlay�p
komut �al��t�rabilir hale gelir.

Kullan�c�n�n komut girmesi gerekti�ini bildirmek amac� ile ekrana 
prompt(uyar�) karakteri '>' yazd�r�l�r. Kullan�c� herhangi bir komut 
girdikten sonra gereken i�lemler yap�l�nca -sonland�rma komutu olan 
C/c komutu girilmedi�i s�rece- tekrar prompt(uyar�) karakteri '>' ekrana 
yazd�r�l�r.

Komutlar b�y�k veya k����k harf olabilir (not case-sensitive).

Devre y�kleme (Y/y) ve ilklendirme(I/i) komutu girilmeden di�er komutlar
(H/h, L/l, S/s, G/g, G*/g*, K/k, C/c) aktifle�memektedir. �ncelikle Y ve I
komutlar�n�n girilmesi gereklidir.

Var olan komutlar d���nda farkl� bir komut girilmeye �al���ld���nda hata
mesaj� ekrana yazd�r�l�r ve kullan�c�dan tekrar komut girilmesi beklenir.

Kullan�c�n�n girdi�i her komut, komut.txt dosyas�na yazd�r�l�r. T�m yap�lan
i�lemler ise tarih/saat kaydedilerek log.txt dosyas�na yazd�r�l�r.

C/c komutu girildi�inde program sonland�r�l�r.

Komutlar 			   ve 		�cralar�
Y <devre.txt> 					�devre.txt� dosyas�ndan devreyi y�kler
I 						�deger.txt� icindeki degerlerle devre ilklendirilir
H <giris ucundan biri/birileri> 		Ilgili u�/u�lar� Lojik-1 yapar
L <giris ucundan biri/birileri> 		Ilgili u�/u�lar� Lojik-0 yapar
S 						Devreyi sim�le eder
G <giris/��k�s ucundan biri/birileri> 		Ilgili u�/u�lar�n seviyesini (0 veya 1) konsolda g�sterir
G* 						T�m u�lar�n seviyesini (0 veya 1) konsolda g�sterir
K <komut.txt> 					�komut.txt� dosyas� i�indeki komutlar� konsoldan oldugu gibi icra eder
C 						 Benzetimden ��k�s yapar
