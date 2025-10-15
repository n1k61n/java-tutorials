**Interface** — Java-da **abstraksiyanı (abstraction)** həyata keçirməyin ikinci yoludur.  
İnterfeys tamamilə **abstrakt sinif** kimidir, lakin bütün metodları **bədəsiz (body-siz)** olur.

---

### 🔹 İnterfeys nədir?

**Interface** — bir neçə sinif arasında **ortaq metod adlarını müəyyən etmək**, amma onların **necə işləyəcəyini** (bədəsini) yazmamaq üçün istifadə olunur.

Yəni interfeys _nə edilməlidir_ deyir, amma _necə edilməlidir_ — onu həyata keçirən (implement edən) sinif müəyyənləşdirir.

---

### 🧩 Sadə nümunə

```java
// İnterfeys
interface Animal {
  public void animalSound(); // bədəsiz metod
  public void sleep();       // bədəsiz metod
}

// İnterfeysi implement edən sinif
class Pig implements Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }

  public void sleep() {
    System.out.println("Zzz");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig();
    myPig.animalSound();
    myPig.sleep();
  }
}
```

📤 **Nəticə:**

```
The pig says: wee wee
Zzz
```

---

### 🔹 Əsas qeydlər

|Qeyd|İzah|
|---|---|
|❌ İnterfeys obyekt yarada bilmir|`Animal myAnimal = new Animal();` → **xəta**|
|⚙️ İnterfeys metodlarının **bədəni yoxdur**|Metodların bədəsini implement edən sinif yazır|
|✅ İnterfeysi implement edən sinif **bütün metodları yenidən yazmalıdır**||
|🌐 İnterfeys metodları avtomatik olaraq **public** və **abstract** sayılır||
|🔒 İnterfeys atributları avtomatik olaraq **public static final** olur||
|🚫 İnterfeys **constructor** ehtiva edə bilməz|Çünki obyekt yarada bilmir|

---

### 🔹 Niyə və nə zaman interfeyslərdən istifadə olunur?

1. **Təhlükəsizlik (Security):**  
    — Həssas detallar gizlədilir, yalnız vacib metod adları göstərilir.
    
2. **Çoxsaylı irslilik (Multiple Inheritance):**  
    — Java-da bir sinif yalnız **bir superclass-dan** irs ala bilər,  
    amma **birdən çox interfeysi** implement edə bilər.
    

---

### 🧱 Bir neçə interfeysi implement etmək

```java
interface FirstInterface {
  public void myMethod();
}

interface SecondInterface {
  public void myOtherMethod();
}

// Bir sinif bir neçə interfeysi implement edə bilər
class DemoClass implements FirstInterface, SecondInterface {
  public void myMethod() {
    System.out.println("Some text..");
  }

  public void myOtherMethod() {
    System.out.println("Some other text...");
  }
}

class Main {
  public static void main(String[] args) {
    DemoClass myObj = new DemoClass();
    myObj.myMethod();
    myObj.myOtherMethod();
  }
}
```

📤 **Nəticə:**

```
Some text..
Some other text...
```

---

### 💡 Abstrakt sinif və interfeys arasındakı fərqlər

|Xüsusiyyət|Abstract Class|Interface|
|---|---|---|
|**Obyekt yaradıla bilər?**|❌ Xeyr|❌ Xeyr|
|**Metodların bədəni ola bilərmi?**|✅ Bəli (bəziləri)|❌ Xeyr (Java 8-dən sonra `default` metod ola bilər)|
|**İrslilik**|Yalnız **bir** sinifdən irs alınır|**Bir neçə interfeys** implement edilə bilər|
|**Atributlar**|Normal ola bilər|Həmişə `public static final`|
|**Açar söz**|`extends`|`implements`|

---

