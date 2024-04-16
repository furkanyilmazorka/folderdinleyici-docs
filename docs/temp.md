``` mermaid
graph TD
    A[Start] --> B{exist}
    B -->|no| C{missing}
    C -->|yes| D[check old files]
    D --> E(spit)
    E --> F(conf)
    B -->|yes| E
```

``` py title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

[Projeye Git](https://github.com/furkanyilmazorka/version){ .md-button .md-button--primary }