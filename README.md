# Python funkcja f(x)
Wyznaczanie typu funkcji oraz wyliczanie podstawowych parametrów.

#KOD PROGRAMU

import math
print("Podaj libczby a, b, c, do funkcji f(x) = ax^2 + bx + c")

a = float(input('Podaj pierwszą liczbę a = '))
b = float(input('Podaj drugą liczbę b = '))
c = float(input('Podaj trzecią liczbę c = '))
if (a == 0 and b != 0 and c != 0):  # funkcja liniowa
    x = c/b
    y = b*x+c
    print("Funkcja liniowa: f(x) =", str(b)+"x +",
          str(c)+", x = "+str(x), "y = "+str(y))
if (a == 0 and b != 0 and c == 0):
    x = c/b
    y = b*x+c
    print("Funkcja liniowa: f(x) =", str(b)+"x"+", x = "+str(x), "y = "+str(y))
if (a != 0 and b == 0 and c == 0):
    delta = (b**2) - 4*a*c
    print("delta =", str(delta))
    if (delta == 0):
        x1 = -b/(2*a)
        x2 = -b/(2*a)
        p = -b/(2*a)
        q = -delta/(4*a)
        print("Funkcja kwadratowa stała: f(x)=", str(a) +
              "x^2 +", str(b)+"x +", str(c)+", x1 =", str(x1), "x2 =", str(x2), "Wpółrędne wierschołka: p =", str(p), "q =", str(q))
if (a != 0 and b != 0):  # funkcja kwadratowa
    delta = (b**2) - 4*a*c
    print("delta =", str(delta))
    if (delta > 0):
        x1 = (-b-math.sqrt(delta))/(2*a)
        x2 = (-b+math.sqrt(delta))/(2*a)
        p = -b/(2*a)
        q = -delta/(4*a)
        print("Funkcja kwadratowa: f(x)=", str(a) +
              "x^2 +", str(b)+"x +", str(c)+", x1 =", str(x1), "x2 =", str(x2), "Wpółrędne wierschołka: p =", str(p), "q =", str(q))
    if (delta == 0):
        x1 = -b/(2*a)
        x2 = -b/(2*a)
        p = -b/(2*a)
        q = -delta/(4*a)
        print("Funkcja kwadratowa: f(x)=", str(a) +
              "x^2 +", str(b)+"x +", str(c)+", x1 =", str(x1), "x2 =", str(x2), "Wpółrędne wierschołka: p =", str(p), "q =", str(q))
    if (delta < 0):
        print("Brak pierwiastków x1, x2")

if (a != 0 and b == 0 and c != 0):  # funkcja stała
    delta = b**2 - 4*a*c
    print("delta =", str(delta))
    if (delta > 0):
        x1 = -b-math.sqrt(delta)/(2*a)
        x2 = -b+math.sqrt(delta)/(2*a)
        p = -b/(2*a)
        q = -delta/(4*a)
        print("Funkcja stała: f(x) =", str(a) + "x^2 +", str(c)+", x1 =", str(x1),
              "x2 =", str(x2), "Wpółrędne wierschołka: p =", str(p), "q =", str(q))
    if (delta == 0):
        x1 = -b/(2*a)
        x2 = -b/(2*a)
        p = -b/(2*a)
        q = -delta/(4*a)
        print("Funkcja stała: f(x) =", str(a) + "x^2 +", str(c)+", x1 =", str(x1),
              "x2 =", str(x2), "Wpółrędne wierschołka: p =", str(p), "q =", str(q))
    if (delta < 0):
        print("Brak pierwiastków x1, x2")

if (a == 0 and b == 0 and c != 0):  # brak funkcji
    print("To nie jest funkcja : f(x)=", str(c))

