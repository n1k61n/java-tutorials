
Metodun yüklənməsi (**Method Overloading**) ilə eyni ada sahib, lakin **fərqli parametrlərə** malik birdən çox metod ola bilər:

Java

```
int myMethod(int x)
float myMethod(float x)
double myMethod(double x, double y)
```

Eyni şeyi etməli olan iki fərqli metod təyin etmək əvəzinə, bir metodu yükləmək daha yaxşıdır.

Aşağıdakı nümunədə, həm **`int`** (tam ədəd), həm də **`double`** (həqiqi ədəd) tipləri üçün işləməsi üçün **`plusMethod`** metodunu yükləyirik:

### Metodun Yüklənməsi Nümunəsi

Java

```
static int plusMethod(int x, int y) {
  // Tam ədədləri toplayır və tam ədəd qaytarır
  return x + y;
}

static double plusMethod(double x, double y) {
  // Həqiqi ədədləri toplayır və həqiqi ədəd qaytarır
  return x + y;
}

public static void main(String[] args) {
  // int parametrləri ilə plusMethod çağırılır
  int myNum1 = plusMethod(8, 5);
  // double parametrləri ilə plusMethod çağırılır
  double myNum2 = plusMethod(4.3, 6.26);
  
  System.out.println("int: " + myNum1);      // Çıxış: int: 13
  System.out.println("double: " + myNum2);   // Çıxış: double: 10.56
}
```

---

**Qeyd:** Birdən çox metod, parametrlərin sayı və/və ya tipi fərqli olduğu müddətcə eyni ada malik ola bilər. Java hansı metodun çağırılacağını, ötürülən arqumentlərin tiplərinə uyğun olaraq müəyyən edir.