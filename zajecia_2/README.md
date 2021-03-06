1. W pliku notatki_2.txt jest szczegółowy plan wykładu.
Kolejmość programów wg wykładu:
    funkcja.py
    funkcja_return.py
    funkcja_argumenty.py
    funkcja_args.py
    funkcja_keyword.py
    funkcja_kwargs.py
    funkcja_wszystko.py
    funkcja_obiektem_pierwszej_kategori.py
    klasa_self.py
    klasa_init.py
    klasa_dziedziczenie.py
    klasa_dziedziczenie_wielokrotne.py
    klasa_dziedziczenie_diament.py

2. W pliku praca_domowa.txt jest jedno zadania domowe, na rozwiązania czekamy do 13.11.2016 włącznie.

3. Praca domowa:

Proszę zaimplementować klasę `Vector`. 
Ta klasa będzie reprezentować wektor o rozmiarze n.
Przykładowe tworzenie instancji klasy:

    Vector(5) # tworzy wektor jednowymiarowy o długości 5 (n = 1)
    Vector(1, 2, 3) # tworzy wektor trójwymiarowy (n = 3)

Instancje klasy Vector powinno dać się zrzutować na stringa:

Wskazówka 1: https://docs.python.org/3/reference/datamodel.html#object.__str__
Wskazówka 2: https://docs.python.org/3/reference/datamodel.html#object.__repr__


    >>> v = Vector(1, 2)
    >>> print(v)
    Vector(1, 2)
    >>> v1 = Vector(2, 4, 5.6, 7,8)
    >>> print(v1)
    Vector(2, 4, 5.6, 7, 8)
    
Powinno dać się porównać czy dwie różne instancje klasy wektor są sobie równe:

Wskazówka 1: https://docs.python.org/3/reference/datamodel.html#object.__eq__

na potrzeby tej pracy domowej proszę założyć, że operacja na wektorach o różnym wymiarze nie wystąpi

    >>> v1 = Vector(1, 2, 3)
    >>> v2 = Vector(1, 2, 3)
    >>> id(v1)
    140449009673384     # dla każdego wywołania id wynik będzie inny
    >>> id(v2)
    140449009673832     # ważne zeby wynik id(v1) był inny niż id(v2)
    >>> v1 is v2
    False
    >>> v1 == v2
    True                # dwa wektory powinny być uznane za równe tylko jeśli mają te same "współrzędne"
    >>> v3 = Vector(1, 2, 4)
    >>> v1 == v3        # dwa wektory z różnymi "współrzędnymi" powinny być uznane za nierówne
    False
    >>> id(v3)
    140449009532152
    
Dodawanie dwóch wektorów o tym samym wymiarze powinno tworzyć nowy wektor o tym samym wymiarze:

Wskazówka: https://docs.python.org/3/reference/datamodel.html#object.__add__

na potrzeby tej pracy domowej proszę założyć, że operacja na wektorach o różnym wymiarze nie wystąpi

    >>> v1 = Vector(1, 2)
    >>> v2 = Vector(3, 4)
    >>> v3 = v1 + v2
    >>> print(v1)
    Vector(1, 2)
    >>> print(v2)
    Vector(3, 4)
    >>> print(v3)
    Vector(4, 6)
    
Mnożenie wektora przez liczbę powinno dawać nowy wektor o tym samym wymiarze z 
odpowiednio przemnożonymi "współrzędnymi":

Wskazówka: https://docs.python.org/3/reference/datamodel.html#object.__mul__

    >>> v = Vector(1.1, 2.2, 3, 4)
    >>> v2 = v * 6
    >>> print(v2)
    Vector(6.6000000000000005, 13.200000000000001, 18, 24)
    >>> print(v)
    Vector(1.1, 2.2, 3, 4)
    
Bonus: Mnożenie liczby przez wektor powinno dawać taki sam wektor jak mnożenie wektora przez liczbę:

Wskazówka: https://docs.python.org/3/reference/datamodel.html#object.__rmul__
    
    >>> v = Vector(1.1, 2.2, 3, 4)
    >>> v2 = v * 6
    >>> print(v2)
    Vector(6.6000000000000005, 13.200000000000001, 18, 24)
    >>> print(v)
    Vector(1.1, 2.2, 3, 4)
    >>> v = Vector(1.1, 2.2, 3, 4)
    >>> v2 = v * 6
    >>> v3 = 6 * v
    >>> print(v)
    Vector(1.1, 2.2, 3, 4)
    >>> print(v2)
    Vector(6.6000000000000005, 13.200000000000001, 18, 24)
    >>> print(v3)
    Vector(6.6000000000000005, 13.200000000000001, 18, 24)
    >>> v2 == v3
    True
    >>> id(v)
    139765753211032
    >>> id(v2)
    139765753541632
    >>> id(v3)
    139765839412472

    
