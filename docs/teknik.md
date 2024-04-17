# Teknik Dökümantasyon

## Akış Diyagramı

``` mermaid
graph TD
    n0(("Başlangıç")) --> n1["Güncelleme Var Mı?"]
    n1 --evet--> n2["Otomatik Güncelleme"] 
    n1 --hayır--> n3["Config var mı?"]
    n2 --> n0
    n3 --evet--> n4["Config Düzgün Mü?"]
    n3 --hayır--> n5["Config Dosyası Oluştur"]
    n5 --> n0
    n4 --evet--> n6["Gönderilmemiş dosyalar var mı?"]
    n4 --hayır--> n0
    n6 --evet--> n7["Dosyaları Gönder"]
    n6 --hayır--> n8["Klasörü dinlemeye başla"]
    n7 --> n8
    n9(("\n Klasöre yeni \n dosya gelme \n durumu")) --> n7
```
