**Java İrsiyyət (Inheritance) (Subclass və Superclass)**

Java-da bir sinifdən digərinə **atributları** və **metodları** **irsən almaq** mümkündür. Biz "irsiyyət konsepsiyasını" iki kateqoriyaya qruplaşdırırıq:

- **Subclass (uşaq):** Başqa bir sinifdən irsən alan sinif.
    
- **Superclass (valideyn):** İrsən alınan sinif.
    

Bir sinifdən irsən almaq üçün **`extends`** açar sözündən istifadə edin.

Aşağıdakı nümunədə, **`Car`** sinfi (**subclass**) **`Vehicle`** sinfindən (**superclass**) atributları və metodları irsən alır:

Java

```
// Superclass (Valideyn Sinif)
class Vehicle {
  protected String brand = "Ford";    // Vehicle atributu
  public void honk() {                 // Vehicle metodu
    System.out.println("Tuut, tuut!");
  }
}

// Subclass (Uşaq Sinif)
class Car extends Vehicle {
  private String modelName = "Mustang"; // Car atributu
  public static void main(String[] args) {
    
    // Car obyektini yaradırıq
    Car myCar = new Car(); 
    
    // Car obyekti Vehicle sinfindən olan honk() metodunu çağırır
    myCar.honk();
    
    // Car obyekti həm öz (modelName), həm də Vehicle sinfindən olan (brand) atributlara daxil olur
    System.out.println(myCar.brand + " " + myCar.modelName); 
    // Çıxış: Ford Mustang
  }
}
```