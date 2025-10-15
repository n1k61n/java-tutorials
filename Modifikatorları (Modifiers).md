
Java-da **modifikatorlar (modifiers)** — siniflərin, atributların, metodların və konstruktorların **giriş səviyyəsini (access level)** və ya **davranışını** müəyyənləşdirmək üçün istifadə olunur.

---

### 🔹 Access Modifiers (Giriş modifikatorları)

Bunlar kodun hansı səviyyədə əlçatan olduğunu (yəni haradan istifadə oluna biləcəyini) idarə edir.

#### **Siniflər (Classes) üçün:**

|Modifier|Təsviri|
|---|---|
|**public**|Sinif bütün digər siniflər tərəfindən əlçatandır.|
|**default** _(modifikator yazılmadıqda)_|Sinif yalnız eyni paketdəki siniflər üçün əlçatandır. (Bu barədə “Packages” mövzusunda daha ətraflı öyrənəcəksiniz.)|

---

#### **Atributlar, metodlar və konstruktorlar üçün:**

|Modifier|Təsviri|
|---|---|
|**public**|Kod bütün siniflər tərəfindən əlçatandır.|
|**private**|Kod yalnız elan olunduğu sinifin içində əlçatandır.|
|**default** _(modifikator yazılmadıqda)_|Kod yalnız eyni paketdəki siniflər tərəfindən əlçatandır.|
|**protected**|Kod eyni paketdəki siniflər və **subclass** (alt siniflər) üçün əlçatandır. (Bunu “Inheritance” mövzusunda öyrənəcəksiniz.)|

---

### 🔹 Non-Access Modifiers (Giriş səviyyəsinə təsir etməyən modifikatorlar)

Bu modifikatorlar kodun giriş səviyyəsini deyil, davranışını dəyişdirir (məsələn, **static**, **final**, **abstract** və s.).  
Onlar barədə ayrıca dərsdə danışılır.

---

### 🧩 Public və Private fərqi (Nümunə)

**Real həyatdan misal:**

- `public` → ictimai park — hər kəs daxil ola bilər
    
- `private` → ev açarınız — yalnız siz istifadə edə bilərsiniz
    

**Kod nümunəsi:**

```java
class Person {
  public String name = "John";   // Public - hər yerdən əlçatan
  private int age = 30;          // Private - yalnız bu sinifin içində əlçatan
}

public class Main {
  public static void main(String[] args) {
    Person p = new Person();
    System.out.println(p.name);   // İşləyir
    System.out.println(p.age);    // Xəta: age private-dir
  }
}
```

---

### 💡 İzah:

Burada `name` **public** olaraq elan edildiyi üçün `Main` sinifindən ona müraciət edilə bilir.  
Ancaq `age` **private** olduğundan yalnız `Person` sinifinin içində istifadə oluna bilər.

---

İstəsən, bu mövzunun **“protected” və “default”** hissəsini ayrıca nümunələrlə də izah edə bilərəm — istəyirsən əlavə edim?