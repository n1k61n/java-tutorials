


Tiplərin dəyişdirilməsi (Type casting) bir məlumat tipini başqa bir tipə çevirmək deməkdir. Məsələn, bir **int** tipini **double** tipinə çevirmək.

Java-da iki əsas tipdə dəyişdirmə (casting) mövcuddur:

---

### 1. Genişləndirən Dəyişdirmə (**Widening Casting**) (avtomatik)

Bu, kiçik ölçülü bir tipi daha böyük ölçülü bir tipə çevirməkdir. Bu, avtomatik olaraq baş verir, çünki heç bir məlumat itkisi riski yoxdur.

Sıralama:

byte → short → char → int → long → float → double

---

### 2. Daraldan Dəyişdirmə (**Narrowing Casting**) (əl ilə)

Bu, böyük ölçülü bir tipi daha kiçik ölçülü bir tipə çevirməkdir. Bu, əl ilə (kodda mötərizədə tip göstərilməklə) edilməlidir, çünki məlumat itkisi riski (məsələn, rəqəmin bir hissəsinin itməsi) mövcuddur.

Sıralama:

double → float → long → int → char → short → byte