**Java Polimorfizm (Polymorphism)**

**Polimorfizm** "çox formalı" deməkdir və bir-biri ilə **irsiyyət** vasitəsilə əlaqəli olan bir çox sinifimiz olduqda baş verir.

Əvvəlki fəsildə qeyd etdiyimiz kimi, **irsiyyət** bizə bir sinifdən atributları və metodları irsən almağa imkan verir. **Polimorfizm** isə həmin metodlardan **fərqli tapşırıqları** yerinə yetirmək üçün istifadə edir. Bu, bizə **tək bir hərəkəti fərqli yollarla** həyata keçirməyə imkan verir.

Məsələn, **`animalSound()`** adlı metodu olan **`Animal`** adında bir **superclass** (valideyn sinif) düşünün. Heyvanların **subclass-ları** (övlad sinifləri) **`Pigs`** (Donuzlar), **`Cats`** (Pişiklər), **`Dogs`** (İtlər), **`Birds`** (Quşlar) ola bilər. Və onların hər biri öz heyvan səsinin fərqli implementasiyasına malikdir (donuz xoruldar, pişik miyoldayar və s.):

Java

```
// Superclass (Valideyn Sinif)
class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

// Subclass 1
class Pig extends Animal {
  // animalSound() metodu Pig sinfi üçün yenidən təyin edilir (override olunur)
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

// Subclass 2
class Dog extends Animal {
  // animalSound() metodu Dog sinfi üçün yenidən təyin edilir (override olunur)
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}

// Əsas İcra
class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();  // Animal obyekti
    Animal myPig = new Pig();        // Pig obyekti Animal kimi referans edilir
    Animal myDog = new Dog();        // Dog obyekti Animal kimi referans edilir

    myAnimal.animalSound(); // Çıxış: The animal makes a sound
    myPig.animalSound();    // Çıxış: The pig says: wee wee
    myDog.animalSound();    // Çıxış: The dog says: bow wow
  }
}
```

Bu nümunədə, **`animalSound()`** metodu eyni ada malikdir, lakin hər fərqli heyvan (övlad sinif) üçün fərqli şəkildə işləyir. Bu, **polimorfizmin** ən bariz nümunələrindən biridir.