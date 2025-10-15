**Polymorphism** — yunanca “çox formalılıq” deməkdir (“poly” = çox, “morph” = forma).  
Java-da **polimorfizm** o zaman baş verir ki, bir neçə sinif **irsilik (inheritance)** vasitəsilə bir-biri ilə əlaqəlidir, lakin **eyni adlı metod** bu siniflərdə **fərqli şəkildə işləyir**.

---

### 🔹 Sadə izah

- **Inheritance** → metod və atributların miras alınmasını təmin edir.
    
- **Polymorphism** → həmin metodların **fərqli şəkildə icra olunmasına** imkan yaradır.
    

Yəni eyni əməliyyatı (“animalSound()” kimi) fərqli obyektlər müxtəlif cür yerinə yetirə bilir.

---

### 🧩 Nümunə

```java
class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}

class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();  // Animal obyekti
    Animal myPig = new Pig();        // Pig obyekti
    Animal myDog = new Dog();        // Dog obyekti

    myAnimal.animalSound();  // "The animal makes a sound"
    myPig.animalSound();     // "The pig says: wee wee"
    myDog.animalSound();     // "The dog says: bow wow"
  }
}
```

📤 **Nəticə:**

```
The animal makes a sound
The pig says: wee wee
The dog says: bow wow
```

---

### 🔹 Necə işləyir?

- `Pig` və `Dog` sinifləri **`Animal` sinifindən extends** vasitəsilə miras alır.
    
- Hər biri `animalSound()` metodunu **özünəməxsus şəkildə yenidən yazır (override edir)**.
    
- Java proqramı **obyektin tipinə görə** (run-time zamanı) uyğun olan metodu çağırır.
    

Bu, **runtime polymorphism** (işləmə zamanı polimorfizm) adlanır.

---

### 🔹 Niyə və nə zaman istifadə olunur?

✅ **Kodun təkrar istifadəsi (Code reusability):**  
Eyni bazadan (`Animal`) fərqli siniflər (`Pig`, `Dog`) yaradıla bilər.

✅ **Kodun çevikliyi (Flexibility):**  
Yeni heyvan sinfi əlavə etdikdə (`Cat`, `Bird` və s.), yalnız `animalSound()` metodunu yazmaq kifayətdir — qalan kodu dəyişməyə ehtiyac yoxdur.

✅ **Təmiz və oxunaqlı struktur:**  
Eyni metod adı ilə müxtəlif davranışlar idarə olunur.

---

### 💡 Sadə müqayisə

|Sinif|Metod|Çıxış|
|---|---|---|
|`Animal`|`animalSound()`|The animal makes a sound|
|`Pig`|`animalSound()`|The pig says: wee wee|
|`Dog`|`animalSound()`|The dog says: bow wow|

---

### 🧠 Qısa nəticə

|Anlayış|Mənası|
|---|---|
|**Inheritance**|Siniflər arasında atribut və metodların miras alınması|
|**Polymorphism**|Miras alınan metodların fərqli cür işləməsi|
|**extends**|İrsilik qurmaq üçün istifadə olunur|
|**override**|Superclass metodunu fərqli şəkildə yenidən yazmaq|
