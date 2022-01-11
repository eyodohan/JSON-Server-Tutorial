# JSON-Server-Tutorial

Kategoriye göre sıralama yapmak istersek "http://localhost:3000/products?category=electronics" şeklinde yazacaz. Filtreleme yapmak istediğimiz özelliği ? nden sonra yazıp = koyuyoruz.


Kategorisi elektronik olup altında discount özelliği olanları göstermek istersek "http://localhost:3000/products?category=electronics&discount.type=shipping" şeklinde yazacaz. "&discount.type=shipping"...


Fiyata göre sıralamak istersek "http://localhost:3000/products?_sort=price". "_sort=price" ibaresini eklememiz gerekiyor. Default olarak ascending olarak sıralıyor.
Descending olarak sıralamak için "http://localhost:3000/products?_sort=price&_order=desc". "_sort=price&_order=desc" ibaresini eklememiz gerekir.
