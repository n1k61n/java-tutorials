

**İnkapsulyasiya** (Encapsulation) əsas mənası **"həssas"** datanın kənar istifadəçilərdən gizlədilməsini təmin etməkdir. Buna nail olmaq üçün aşağıdakılar tələb olunur:

1. Sinif dəyişənlərini/atributlarını **`private`** elan etmək.
    
2. **`private`** dəyişənin dəyərinə daxil olmaq və onu yeniləmək üçün **`public`** **`get`** və **`set`** metodları təmin etmək.
    

---

## Get və Set Metodları

Əvvəlki fəsillərdən bildiyiniz kimi, **`private`** dəyişənlərə yalnız eyni sinif daxilində daxil olmaq mümkündür (kənar sinfin ona girişi yoxdur). Lakin, **`public`** **`get`** və **`set`** metodlarını təmin etsək, onlara daxil olmaq mümkün olur.

- **`get`** metodu dəyişənin dəyərini **geri qaytarır** (returns).
    
- **`set`** metodu isə dəyişənin dəyərini **təyin edir** (sets).
    

### Sintaksis

Hər iki metodun sintaksisi **`get`** və ya **`set`** ilə başlayır, ardınca isə **dəyişənin adının ilk hərfi böyük hərflə** yazılmış forması gəlir:

|Metod Tipi|Sintaksis Nümunəsi|Məqsəd|
|---|---|---|
|**Get**|`getName()`|`name` dəyişəninin dəyərini qaytarır|
|**Set**|`setName(String newName)`|`name` dəyişəninin dəyərini yeniləyir|