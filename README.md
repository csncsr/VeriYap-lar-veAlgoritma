# VeriYapilariVeAlgoritma
## Merge Sort Projesi

[16,21,11,8,12,22]

(Array olabildiğince ayrıştırılır)
[22,27,16]  [2,18,6] 

(Ortadan ikiye böldükten sonra sol tarafta kalanları öncelikle sıralayabiliriz)
[22,27] [16]  [2,18,6]
[22] [27] [16]  [2,18,6]

(22 ve 27'den minimum olan hangisi seçilir ve solda kalacak şekilde yazılır.)
[22,27] [16]  [2,18,6]

(Ardından [22,27] ve [16] arrayleri arasında hangisinin ilk değeri küçük o seçilir. Bu örnekte [16]'yı seçtiğimizde o array tamamen boşalacak)
[16, , ]   [2,18,6]
[22,27] []  

(Sıralarken karşılaştırdığımız array listelerinden birisi boş kaldığına göre diğerlerini sırasıyla peşine yazabiliriz)
[16,22,27]  [2,18,6]

(Ayrıştırdığımız kısmın sağına geçebiliriz)
[16,22,27]  [2,18] [6]
[16,22,27]  [2] [18] [6]

([2] ve [18] arasından hangisinin daha küçük olduğuna karar verilir ve sıralanmış hali yazılır. Bizim örneğimizde [2] küçük)
[16,22,27]  [2,18] [6]

([16,18] ve [6] arrayleri arasında hangisinin ilk değeri küçük o seçilir. Bu örnekte [2,18]'in ilk değeri olan "2" < "6")
[16,22,27]  [2, , ]
[16,22,27]  [ ,18] [6]

("2" değerini yerleştirdikten sonra, tekrardan sorgu çalışıyor ve "18" mi küçük yoksa "6" mı kontrol ediliyor. Bu sorguda "6" daha küçük)
[16,22,27]  [2,6, ]
[16,22,27]  [ ,18] []

(Bir array tamamen boşaldı, diğerinde ise sadece 18 kaldı. 18'i de en sağa yazabiliriz)
[16,22,27]  [2,6,18]

(Ayrıştırdığımız arrayi şimdi sırasıyla karşılaştırarak dizmeye başlayabiliriz)
[ , , , , , ]
[16,22,27]  [2,6,18]

(İki arrayin de en soldaki değerleri kıyaslanıyor ve küçük olan başa yazılıyor. "2"<"16" olduğu için 2 en başa yazılır)
[2, , , , , ]
[16,22,27]  [ ,6,18]

(Sorgu tekrarlanır ve "6"<"16" olduğu için 6'yı yazarız)
[2,6, , , , ]
[16,22,27]  [ , ,18]

(Sorgu tekrarlanır ve "16"<"18" olduğundan 16'yı üçüncü sıraya yazarız)
[2,6,16, , , ]
[ ,22,27]  [ , ,18]

(Sorgu tekrarlandığında "18"<"22" olduğu için 18'i yazarız)
[2,6,16,18, , ]
[ ,22,27]  [ , , ]

(Bir array tamamen boşaldığına göre geri kalanı peş peşe yazabiliriz)
[2,6,16,18,22,27]

Big-O = n(logn)
