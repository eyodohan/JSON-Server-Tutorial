# JSON-Server-Tutorial

Kategoriye göre sıralama yapmak istersek "http://localhost:3000/products?category=electronics" şeklinde yazacaz. Filtreleme yapmak istediğimiz özelliği ? nden sonra yazıp = koyuyoruz.


Kategorisi elektronik olup altında discount özelliği olanları göstermek istersek "http://localhost:3000/products?category=electronics&discount.type=shipping" şeklinde yazacaz. "&discount.type=shipping"...


Fiyata göre sıralamak istersek "http://localhost:3000/products?_sort=price". "_sort=price" ibaresini eklememiz gerekiyor. Default olarak ascending olarak sıralıyor.
Descending olarak sıralamak için "http://localhost:3000/products?_sort=price&_order=desc". "_sort=price&_order=desc" ibaresini eklememiz gerekir.


Hem fiyata göre sıralamak hem de kategori ismini alfabetik sıralamak için "http://localhost:3000/products?_sort=price,category&_order=desc,asc"  "products?_sort=price,category&_order=desc,asc" ibaresini ekleriz ve bu şekilde fiyatı aynı olan ürünler varsa sıralaması alfabetik olur.


Default olarak 10 adet ürün gösterilir "http://localhost:3000/products?_page" . Ancak sayfada gösterilecek ürünleri limitleyebiliriz. "http://localhost:3000/products?_page=1&_limit=2". Artık her sayfada 2 şer adet ürün gösterilir.


NOT: Eğer tarayıcının devtools unu açarsak network sekmesinde istek yaptığımızda son sayfa ilk sayfa gibi linkler oluşturulur.


Eğer ürünleri fiyatı 2000 ile 6000 arasında olanlara göre sıralamak istersek "http://localhost:3000/products?price_gte=2000&price_lte=6000" adresini kullanırız.
"/products?price_gte=2000&price_lte=6000". 

Not equal ile de ürünleri sergileyebiliriz. "http://localhost:3000/products?id_ne=1" adresi ile id si 1 olan hariç ürünler sergilenir.

Yine kategorisi f ile başlayanları sergilemek için. "http://localhost:3000/products?category_like=^f"  "/products?category_like=^f" like operatörünü kullanırız.


Full text search yapmak için "http://localhost:3000/products?q=1000" "?q=..." şeklinde kullanırız
