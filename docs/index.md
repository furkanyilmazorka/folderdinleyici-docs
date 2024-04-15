# Anasayfa

## Folderdinleyici nedir?

Folderdinleyici belirlediğiniz klasörü dinleyip içeri koyulan dosyaları belirlediğniz SFTP sunucusuna gönderir.

Tek yönlü çalışan bir senkronizasyon programı gibi düşünülebilinir.

## Nasıl kullanılır?



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

``` mermaid
graph LR
  A[Start] --> B{Error?};
  B -->|Yes| C[Hmm...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Yay!];
```

``` py title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

[Projeye Git](https://github.com/furkanyilmazorka/version){ .md-button .md-button--primary }