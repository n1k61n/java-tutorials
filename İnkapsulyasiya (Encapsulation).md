

**Encapsulation** (kapsullaşdırma) — **həssas (məxfi) məlumatların istifadəçilərdən gizlədilməsi** prinsipidir.  
Bu, obyekt yönümlü proqramlaşdırmanın (OOP) əsas anlayışlarından biridir.

---

### 🔹 Kapsullaşdırmanın məqsədi

Məqsəd odur ki, sinifin daxilindəki dəyişənlərə (atributlara) **birbaşa müdaxilə olmasın**, yalnız müəyyən metodlar vasitəsilə (get və set) dəyişdirilə bilsin.

---

### 🔹 Bunu etmək üçün:

1. Sinifin dəyişənlərini (`attributes`) **private** kimi elan et.  
    → Beləcə, onlar yalnız həmin sinifin içərisində əlçatan olacaq.
    
2. Dəyişənlərə nəzarətli giriş üçün **public get** və **set** metodları yarat.
    

---

### 🔹 Get və Set metodları

- **get** → dəyişənin dəyərini geri qaytarır.
    
- **set** → dəyişənin dəyərini təyin edir.
    

Adətən, metod adları dəyişənin adının baş hərfi böyük olmaqla belə yazılır:  
**getName()**, **setName()**

---

### 🧩 Nümunə

```java
public class Person {
  private String name; // private = birbaşa giriş qadağandır

  // Getter (dəyəri oxumaq üçün)
  public String getName() {
    return name;
  }

  // Setter (dəyəri dəyişmək üçün)
  public void setName(String newName) {
    this.name = newName;
  }
}
```

---

### 🔹 İzah

- `name` dəyişəni **private** olduğuna görə sinifdən kənarda istifadə oluna bilməz.
    
- Amma **getName()** və **setName()** metodları vasitəsilə bu dəyişənə nəzarətli şəkildə giriş mümkündür.
    

---

### 🚫 Səhv nümunə (birbaşa giriş cəhdi)

```java
public class Main {
  public static void main(String[] args) {
    Person myObj = new Person();
    myObj.name = "John";  // Xəta
    System.out.println(myObj.name); // Xəta
  }
}
```

➡ Kompilyator xətası:

```
error: name has private access in Person
```

---

### ✅ Doğru istifadə

```java
public class Main {
  public static void main(String[] args) {
    Person myObj = new Person();
    myObj.setName("John");              // Dəyəri təyin edir
    System.out.println(myObj.getName()); // Dəyəri oxuyur
  }
}
```

**Nəticə:**

```
John
```

---

### 💡 Niyə Kapsullaşdırma Vacibdir?

1. ✅ **Məlumat üzərində daha yaxşı nəzarət**  
    – Hansı dəyişənin oxunub/yazılacağını sən müəyyən edirsən.
    
2. 🔒 **Təhlükəsizlik**  
    – Həssas məlumatları birbaşa dəyişmək mümkün olmur.
    
3. ⚙️ **Elastiklik**  
    – Kodun bir hissəsini dəyişdirmək digər hissələrə təsir etmir.
    
4. 🔁 **Yalnız oxuma/yazma rejimi**  
    – Yalnız `get` varsa → dəyişən **read-only** olur.  
    – Yalnız `set` varsa → dəyişən **write-only** olur.
    

---
