**Abstraksiya (Data Abstraction)** — istifadəçidən **lazımsız detalların gizlədilməsi** və yalnız **vacib məlumatların göstərilməsi** prosesidir.  
Yəni obyektin necə işlədiyini deyil, **nə etdiyini** göstəririk.

---

### 🔹 Abstraksiyanın məqsədi

Abstraksiya proqramda **məlumatın təhlükəsizliyini artırır**, **sadelik** və **idarəetmə rahatlığı** yaradır.  
Java-da abstraksiyanı iki yolla əldə etmək olar:

1. **Abstract classes** (abstrakt siniflər)
    
2. **Interfaces** (interfeyslər – növbəti mövzuda izah ediləcək)
    

---

### 🔹 `abstract` açar sözü

`abstract` — **non-access modifier**-dır (yəni giriş səviyyəsini deyil, sinifin davranışını müəyyənləşdirir).

#### İstifadəsi:

- **abstract class** → obyekt yaradıla bilməz, yalnız miras alına bilər.
    
- **abstract method** → yalnız abstrakt sinifdə ola bilər və **bədəni (body)** yoxdur.  
    Bədəni **subclass** təmin edir (yəni miras alan sinif yazır).
    

---

### 🧩 Nümunə

```java
// Abstrakt sinif
abstract class Animal {
  // Abstrakt metod (bədəni yoxdur)
  public abstract void animalSound();

  // Normal metod (bədəni var)
  public void sleep() {
    System.out.println("Zzz");
  }
}

// Subclass (Animal sinfindən irs alır)
class Pig extends Animal {
  // Abstrakt metodu burada reallaşdırırıq
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig();  // Pig obyekti yaradılır
    myPig.animalSound();    // "The pig says: wee wee"
    myPig.sleep();          // "Zzz"
  }
}
```

📤 **Nəticə:**

```
The pig says: wee wee
Zzz
```

---

### 🔹 Əhəmiyyətli qeydlər

- `Animal myObj = new Animal();` ❌ → **xəta verəcək**, çünki abstrakt sinifdən **birbaşa obyekt** yaradıla bilməz.
    
- Abstrakt siniflər **miras (inheritance)** vasitəsilə istifadə olunur.
    

---

### 🔹 Niyə və nə zaman istifadə olunur?

✅ **Təhlükəsizlik (Security):**  
Daxili detalları gizlədərək yalnız vacib metodları göstərmək mümkündür.

✅ **Strukturlaşdırma (Organization):**  
Ümumi xüsusiyyətlər abstrakt sinifdə toplanır, fərqli davranışlar isə alt siniflərdə reallaşdırılır.

✅ **Kodun təmizliyi və çevikliyi:**  
Hər yeni sinif eyni abstrakt metodu fərqli cür icra edə bilər — bu, **Polymorphism** ilə birlikdə işləyir.

---

### 💡 Sadə müqayisə

| Anlayış            | Təsviri                                           | Mümkünmü obyekt yaratmaq? |
| ------------------ | ------------------------------------------------- | ------------------------- |
| **Class**          | Normal sinif, bütün metodların bədəni var         | ✅ Bəli                    |
| **Abstract Class** | Bəzi metodları bədəsiz, yalnız miras verilə bilər | ❌ Xeyr                    |
| **Interface**      | Tamamilə abstrakt metodlardan ibarət struktur     | ❌ Xeyr                    |

---
