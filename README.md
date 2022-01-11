# JSON-Server-Tutorial

Kategoriye göre sıralama yapmak istersek "http://localhost:3000/products?category=electronics" şeklinde yazacaz. Filtreleme yapmak istediğimiz özelliği ? nden sonra yazıp = koyuyoruz.


Kategorisi elektronik olup altında discount özelliği olanları göstermek istersek "http://localhost:3000/products?category=electronics&discount.type=shipping" şeklinde yazacaz. "&discount.type=shipping"...


Fiyata göre sıralamak istersek "http://localhost:3000/products?_sort=price". "_sort=price" ibaresini eklememiz gerekiyor. Default olarak ascending olarak sıralıyor.
Descending olarak sıralamak için "http://localhost:3000/products?_sort=price&_order=desc". "_sort=price&_order=desc" ibaresini eklememiz gerekir.


Hem fiyata göre sıralamak hem de kategori ismini alfabetik sıralamak için "http://localhost:3000/products?_sort=price,category&_order=desc,asc"  "products?_sort=price,category&_order=desc,asc" ibaresini ekleriz ve bu şekilde fiyatı aynı olan ürünler varsa sıralaması alfabetik olur.


Default olarak 10 adet ürün gösterilir "http://localhost:3000/products?_page" . Ancak sayfada gösterilecek ürünleri limitleyebiliriz. "http://localhost:3000/products?_page=1&_limit=2". Artık her sayfada 2 şer adet ürün gösterilir.
