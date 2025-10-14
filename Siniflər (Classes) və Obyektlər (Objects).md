
Java obyekt yönümlü proqramlaşdırma dilidir.

Java-da hər şey **siniflər** və **obyektlər**, həmçinin onların **atributları** (xüsusiyyətləri) və **metodları** (davranışları) ilə əlaqələndirilir. Məsələn: real həyatda **avtomobil** bir **obyektdir**. Avtomobilin **atributları** (məsələn, çəkisi və rəngi) və **metodları** (məsələn, sürmək və əyləc etmək) var.

**Sinif** obyekt konstruktoru və ya obyektləri yaratmaq üçün **"şablon"** kimidir.

---

## Sinif Yaratmaq

Sinif yaratmaq üçün **`class`** açar sözündən istifadə edin.

Aşağıdakı nümunədə biz **`x`** adlı bir dəyişənə malik **`Main`** adlı bir sinif yaradırıq:

**`Main.java`**

Java

```
public class Main {
  int x = 5;
}
```

> **Yadda saxlayın:** Java Sintaksis fəslindən bildiyiniz kimi, sinif həmişə böyük hərflə başlamalı və Java faylının adı sinfin adı ilə eyni olmalıdır.

---

## Obyekt Yaratmaq

Java-da obyekt bir sinifdən yaradılır. Biz artıq **`Main`** adlı sinfi yaratmışıq, buna görə indi ondan obyektlər yaratmaq üçün istifadə edə bilərik.

**`Main`** sinfinin obyektini yaratmaq üçün sinif adını, ardınca obyekt adını göstərin və **`new`** açar sözündən istifadə edin:

#### Nümunə

**`myObj`** adlı bir obyekt yaradın və `x` dəyərini çap edin:

Java

```
public class Main {
  int x = 5;

  public static void main(String[] args) {
    // Main sinfindən myObj adlı bir obyekt yaradılır
    Main myObj = new Main();
    
    // Obyekt vasitəsilə x atributuna daxil olub çap edirik
    System.out.println(myObj.x); // Çıxış: 5
  }
}
```