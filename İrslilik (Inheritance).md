
**Inheritance** — Java-da bir sinifin (class) digər sinifdən **xüsusiyyətləri (atributlar) və metodları miras alması** deməkdir.  
Bu, **obyekt yönümlü proqramlaşdırmanın** əsas prinsiplərindən biridir və **kodun təkrar istifadəsini (code reusability)** təmin edir.

---

### 🔹 Əsas anlayışlar

- **Superclass (ata sinif)** — xüsusiyyətləri miras verilən sinif.
    
- **Subclass (övlad sinif)** — həmin xüsusiyyətləri miras alan sinif.
    

İrslilik yaratmaq üçün **`extends`** açar sözündən istifadə olunur.

---

### 🧩 Nümunə

```java
class Vehicle {
  protected String brand = "Ford";   // Vehicle atributu
  public void honk() {               // Vehicle metodu
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle {           // Car sinfi Vehicle-dən irs alır
  private String modelName = "Mustang";

  public static void main(String[] args) {
    // myCar obyekti yaradılır
    Car myCar = new Car();

    // Vehicle sinifindən gələn metodu çağırır
    myCar.honk();

    // brand (Vehicle-dən) və modelName (Car-dan) atributlarını göstərir
    System.out.println(myCar.brand + " " + myCar.modelName);
  }
}
```

📤 **Nəticə:**

```
Tuut, tuut!
Ford Mustang
```

---

### 🔹 `protected` modifikatoru

`Vehicle` sinifindəki `brand` atributu **protected** elan edilib.  
Bu o deməkdir ki:

- həmin atribut eyni paketdəki və **irs alan (subclass)** siniflərdə əlçatandır,
    
- amma **private** olsaydı, `Car` sinifində istifadə etmək mümkün olmazdı.
    

---

### 🔹 Niyə və nə zaman irslilikdən istifadə olunur?

✅ **Kodun təkrar istifadəsi (Reusability):**  
Yeni sinif yaradarkən artıq mövcud olan atributları və metodları yenidən yazmadan istifadə etmək mümkündür.

Məsələn:

- `Vehicle` → ümumi atributlar və metodlar
    
- `Car`, `Bike`, `Bus` → bu xüsusiyyətləri miras alır və özlərinə xas funksiyalar əlavə edirlər.
    

---

### 🧱 `final` açar sözü

Əgər bir sinifin irs alınmasını istəmirsinizsə, onu **`final`** kimi elan edin.

```java
final class Vehicle {
  // ...
}

class Car extends Vehicle {  // Xəta verəcək!
  // ...
}
```

📛 **Nəticə:**

```
error: cannot inherit from final Vehicle
```

---

### 💡 Qısa xülasə

|Termin|Mənası|Misal|
|---|---|---|
|**Superclass**|İrs verilən sinif|`Vehicle`|
|**Subclass**|İrs alan sinif|`Car extends Vehicle`|
|**extends**|İrsliliyi qurur|`class Car extends Vehicle`|
|**protected**|Subclass üçün əlçatan atribut|`protected String brand`|
|**final**|İrsliliyi qadağan edir|`final class Vehicle`|

---

İstəyirsənsə, mən sənə bu nümunəyə **Polymorphism (Çoxformallıq)** hissəsini də əlavə edib göstərə bilərəm — irsli metodların necə fərqli davranış göstərdiyini izah edim?