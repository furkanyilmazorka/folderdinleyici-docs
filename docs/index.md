# Kullanma Kılavuzu

## Folderdinleyici nedir?

<figure markdown="span">
  ![](https://files.catbox.moe/f0nbyp.avif){ width="600" loading=lazy }
  <figcaption>Programa ait ekran görüntüsü</figcaption>
</figure>

Folderdinleyici belirlediğiniz klasörü dinleyip içerisine koyulan dosyaları belirlediğniz SFTP sunucusuna gönderir.

Tek yönlü çalışan bir senkronizasyon programı gibi düşünülebilinir.

## Nasıl kullanılır?

1. Exeyi indirin.     
[İndirmek için tıklayınız.](https://github.com/furkanyilmazorka/version/releases/download/1.0.1.4/folderdinleyici.exe){.md-button}

2. Çift tıklayarak çalıştırın. 
Uygulamayı ilk kez çalıştırdığınızda bulunduğunuz dizine `config.json` isminde bir konfigürasyon dosyası oluşturulacaktır.
Uygulamayı şimdilik kapatabilirsiniz.
Konfigürasyon dosyasının içeriği şuna benzemektedir:
``` json
{
  "Host": "192.168.1.200",
  "Port": 22,
  "Username": "tester",
  "Password": "password",
  "FolderPath": "C:\\Users\\furka\\OneDrive\\Masaüstü\\data",
  "Suffix": "sent-"
}
```
3. SFTP sunucunuzun bilgilerine göre Host, Port, Username ve Password alanlarını doldurunuz. 
4. Dinlenmesini istediğiniz klasörün yolunu aşağıdaki uyarıyı dikkate alarak FolderPath alanına yazınız.
    
    !!! warning "Uyarı"
        Konfigürasyon dosyası JSON olduğu için Windows klasör yolunda bulunan ters eğik çizgi \ karakteri iki kere konulmalıdır!
    
        Örneğin:
    
        Yolumuz: `C:\Users\furka\Projects` ise şu hale getirilmelidir: `C:\\Users\\furka\\Projects`

5. Suffix parametresi opsiyoneldir. 
Görevi gönderilen dosyaların tekrar tekrar gönderilmemesi için dosyaların başına eklenen takı kelimesidir. 
Örneğin: `Fatura.pdf` dosyası eğer başarılı bir şekilde gönderildiyse. `sent-Fatura.pdf` olarak isimlendirilir. 
6. Uygulamayı şimdi tekrar çalıştırdığınızda belirlediğiniz klasördeki dosyaları karşı tarafa aktarmaya başlar ve klasörü gelecekteki potansiyel dosyalar için dinlemeye başlar. 