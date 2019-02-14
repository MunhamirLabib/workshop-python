# minggu-07

Object Oriented Programming(OOP) merupakan suatu konsep pemrograman yang menekankan pada paradigma atau cara pandang terhadap suatu masalah berdasarkan "object".
Dalam konsep OOP semua yang ada didunia ini adalah object dan direpresentasikan dalam bentuk object.
Ditulisan ini kita tidak akan membahas teori OOP, yang akan dibahas hanya langsung cara implementasi konsep OOP pada Python.

Class
Pada konsep pemrograman berbasis object, anda tidak akan asing lagi mendengar istilah class, object, attribute, behaviour, inheritance, dll.
Semua itu pasti akan anda temui disemua bahasa pemrograman yang support OOP. Jika dianalogikan, class merupakan suatu tubuh dari OOP.
Class merupakan abstraksi atau blueprint yang mendefinisikan suatu object tertentu. Class akan menampung semua attribute dan perilaku dari object itu.
Berikut contoh implementasi class pada Python:
class Car:

    color = 'black'
    transmission = 'manual'

    def __init__(self, transmission):
        self.transmission = transmission
        print('Engine is ready!')

    def drive(self):
        print('Drive')

    def reverse(self):
        print('Reverse. Please check your behind.')
Jika diperhatikan, dalam class Car terdapat 2 attribute yaitu color = 'black', transmission = 'manual' dan method yaitu drive(), reverse().
Method dalam konsep OOP mewakili suatu 'behaviour' dari class atau object itu sendiri. Kita akan bahas lebih detail mengenai method.
