# a11yjson
test 04

## Raport

Element "**raport**" zawiera tablicę obiektów. 
Każdy obiekt składa się z:
* **op** - operatora
  * dostępne wartości to:
    * eq - równy (ang: equal)
    * gt - większy niż (ang: greater than)
    * lt - mniejszy niż (ang: less than)
    * gteq - większy lub równy
    * lteq - mniejszy lub równy
* **cond** - warunek
  * przykład `{"op":"eq", "cond":2}` oznacza że warunek będzi spełniony jeśli wartość będzie równa 2
* **info** - informacja tekstowa jeśli warunek jest spełniony
