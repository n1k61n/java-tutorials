**Enum**, sabitlər (dəyişməz dəyişənlər) qrupunu təmsil edən xüsusi bir “sinifdir”.  
`enum` yaratmaq üçün `enum` açar sözündən istifadə olunur (`class` və ya `interface` əvəzinə) və sabitlər vergüllə ayrılır.  
Qeyd: adətən sabitlər **böyük hərflərlə** yazılır.

---

### 💡 Nümunə:

```java
enum Level {
  LOW,
  MEDIUM,
  HIGH
}
```

Enum sabitlərinə **nöqtə (.)** ilə müraciət olunur:

```java
Level myVar = Level.MEDIUM;
```

**Enum** sözü “**enumerations**” ifadəsinin qısaltmasıdır, mənası isə “**xüsusi siyahıya alınmış dəyərlər**” deməkdir.

---

### 🧩 Sinif daxilində Enum

Enum-u sinifin içərisində də yarada bilərsən:

```java
public class Main {
  enum Level {
    LOW,
    MEDIUM,
    HIGH
  }

  public static void main(String[] args) {
    Level myVar = Level.MEDIUM; 
    System.out.println(myVar);
  }
}
```

**Nəticə:**

```
MEDIUM
```

---

### 🧠 Enum və switch operatoru

Enum-lar tez-tez `switch` operatorunda istifadə olunur, çünki onların müəyyən dəyərləri var:

```java
enum Level {
  LOW,
  MEDIUM,
  HIGH
}

public class Main {
  public static void main(String[] args) {
    Level myVar = Level.MEDIUM;

    switch(myVar) {
      case LOW:
        System.out.println("Aşağı səviyyə");
        break;
      case MEDIUM:
        System.out.println("Orta səviyyə");
        break;
      case HIGH:
        System.out.println("Yüksək səviyyə");
        break;
    }
  }
}
```

**Nəticə:**

```
Orta səviyyə
```

---

### 🔁 Enum-lar üzərində dövr (loop)

Enum tiplərinin `values()` adlı bir metodu var.  
Bu metod bütün enum sabitlərini massiv (array) şəklində qaytarır.  
Bu, bütün dəyərləri bir-bir ekrana çıxarmaq üçün faydalıdır:

```java
for (Level myVar : Level.values()) {
  System.out.println(myVar);
}
```

**Nəticə:**

```
LOW
MEDIUM
HIGH
```

---

### ⚖️ Enum və Class arasındakı fərqlər

- Enum da class kimi **atributlara** və **metodlara** malik ola bilər.
    
- Fərq ondadır ki, enum sabitləri **public**, **static** və **final**-dır (dəyişdirilə bilməz).
    
- Enum ilə **obyekt yaratmaq mümkün deyil** (`new` ilə istifadə edilə bilməz).
    
- Enum **başqa sinifdən miras ala bilməz**, amma **interface**-ləri **implement** edə bilər.
    

---

### 🧩 Nə vaxt Enum istifadə etməli?

Enum-lar o hallarda istifadə olunur ki,  
dəyərlər **dəyişməz** və **məlum** olsun, məsələn:

- Ay günləri
    
- Həftə günləri
    
- Rənglər
    
- Kart dəstləri və s.
    

---

