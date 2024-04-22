# Teknik Dökümantasyon

## Akış Diyagramı

``` mermaid
graph TD
    n0(("Başlangıç")) --> n1{"Güncelleme \n Var Mı?"}
    n1 --hayır--> n3{"Config var mı?"}
    n1 --evet--> n2["Otomatik \n Güncelleme "]
    n2 --> n0
    n3 --evet--> n4{"Config \n Düzgün Mü?"}
    n3 --hayır--> n5["Config Dosyası Oluştur"]
    n5 --> n0
    n4 --evet--> n6{"Gönderilmemiş \n dosyalar \n var mı?"}
    n4 --hayır--> n0
    n6 --evet--> n7["Dosyaları Gönder"]
    n6 --hayır--> n8["Klasörü dinle"]
    n7 --> n8
    n8 --> n9{"Yeni dosya \n geldi mi?"}
    n9 --hayır--> n8
    n9 --evet--> n7
```