
**Data abstraksiyası** (Data abstraction) müəyyən detalları gizlətmək və istifadəçiyə yalnız **əsas məlumatı** göstərmək prosesidir.

Abstraksiya ya **abstrak siniflər** (**abstract classes**), ya da **interfeyslər** (**interfaces**) (hansı ki, növbəti fəsildə daha ətraflı öyrənəcəksiniz) vasitəsilə əldə edilə bilər.

**`abstract`** açar sözü siniflər və metodlar üçün istifadə edilən bir **qeyri-giriş dəyişdiricisidir** (non-access modifier):

---

## 1. Abstrak Sinif (Abstract Class) 🧱

Abstrak sinif **obyektlər yaratmaq üçün istifadə oluna bilməyən** qadağan olunmuş sinifdir (ona daxil olmaq üçün **mütləq başqa bir sinif tərəfindən irsən alınmalıdır**).

### Xüsusiyyətləri

- Abstrak sinif həm **abstrak**, həm də **normal** metodlara malik ola bilər.
    
- Bir sinfi **`abstract`** açar sözü ilə elan edirsiniz.
    

---

## 2. Abstrak Metod (Abstract Method) 👻

Abstrak metod yalnız **abstrak sinifdə** istifadə edilə bilər və onun **gövdəsi yoxdur** (gövdəsi **bədəni yoxdur** – _yəni implementasiyası mövcud deyil_).

### Xüsusiyyətləri

- Metodun gövdəsi (**implementasiyası**) **subclass** (irsən alan sinif) tərəfindən təmin edilir.
    

#### Nümunə:

Java

```
// Abstract Sinif
abstract class Animal {
  // Normal (abstrak olmayan) metod
  public void sleep() {
    System.out.println("Zzz");
  }

  // Abstrak metod (gövdəsiz)
  public abstract void animalSound(); 
}

// Subclass (övlad sinif)
class Pig extends Animal {
  // Abstrak metodun gövdəsi burada təmin edilir
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}
```