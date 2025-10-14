**Metod** (və ya **funksiya**) yalnız çağırıldığı zaman işə düşən bir kod blokudur.

Siz metodlara **parametrlər** kimi tanınan məlumatları ötürə bilərsiniz.

Metodlar müəyyən hərəkətləri yerinə yetirmək üçün istifadə olunur.

### Niyə Metodlardan İstifadə Edilməlidir?

Kod təkrar istifadəsi üçün: kodu bir dəfə müəyyənləşdirin və ondan dəfələrlə istifadə edin.

---

### Metodun Yaradılması

Bir metod **sinfin (class)** daxilində elan edilməlidir. O, metodun adı, ardınca dairəvi mötərizələr **`()`** ilə müəyyən edilir. Java bəzi əvvəlcədən müəyyən edilmiş metodlar təqdim edir, məsələn, **`System.out.println()`**, lakin siz müəyyən hərəkətləri yerinə yetirmək üçün öz metodlarınızı da yarada bilərsiniz:

#### Nümunə

**`Main`** sinfinin daxilində bir metod yaradılması:

Java

```
public class Main {
  static void myMethod() {
    // icra olunacaq kod
  }
}
```

#### Nümunənin İzahı

- **`myMethod()`** metodun adıdır.
    
- **`static`** o deməkdir ki, bu metod **`Main`** sinfinə aiddir və **`Main`** sinfinin bir **obyektinə** yox. (Obyektlər və metodlara obyektlər vasitəsilə necə daxil olmaq barədə daha sonra öyrənəcəksiniz.)
    
- **`void`** o deməkdir ki, bu metodun **geri qaytarılan dəyəri (return value)** yoxdur. (Geri qaytarılan dəyərlər haqqında bu fəslin sonrakı hissələrində daha ətraflı öyrənəcəksiniz.)