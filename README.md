# CalculadoraPython
Calculadora básica.

# Herencia.
class Calculadora:
    def __init__(self, numero):
        self.n = numero
        self.datos = [0 for i in range(numero)]

    def ingresar_dato(self):
        self.datos = [int(input("Ingresar datos " + str(i + 1) + " = ")) for i in range(self.n)]

class operaciones_basicas(Calculadora):
    def __init__(self):
        Calculadora.__init__(self, 2)

    def suma(self):
        a, b, = self.datos
        s = a + b
        print(f"El resultado es:{s}")

    def resta(self):
        a, b, = self.datos
        r = a - b
        print(f"El resultado es:{r}")

    def multi(self):
        a, b, = self.datos
        m = a * b
        print(f"El resultado es:{m}")

    def div(self):
        a, b, = self.datos
        d = a / b
        print(f"El resultado es:{d}")

class Raiz(Calculadora):
    def __init__(self):
        Calculadora.__init__(self, 1)

    def cuadrada(self):
        import math
        a, = self.datos
        print(f"El resultado es:{math.sqrt(a)}")


ejemplo = operaciones_basicas()
print(ejemplo.ingresar_dato())
print(ejemplo.multi())
print(ejemplo.div())

ejemplo2 = Raiz()
print(ejemplo2.ingresar_dato())
print(ejemplo2.cuadrada())
