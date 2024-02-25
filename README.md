# Serie-Fibonacci

class FibonacciSt:

    def __init__(self, n):
        self.n = n

    def fib(self):
        fibo = [0, 1]

        for i in range(2, self.n):
            fibo.append(fibo[-1] + fibo[-2])

        return fibo

    def suc_fib(self):
        if self.n <= 0:
            return "N debe ser un entero positivo mayor que cero."
        elif self.n == 1:
            return 0
        elif self.n == 2:
            return 1
        else:
            fibo = self.fib()
            return fibo[-1]


n = int(input("Ingrese el valor de n para la secuencia de Fibonacci: "))
fibonacci = FibonacciSt(n)

print("La secuencia de Fibonacci hasta el término {} es:".format(n))
print(fibonacci.fib())

print("El término número {} de la secuencia de Fibonacci es: {}".format(n, fibonacci.suc_fib()))
