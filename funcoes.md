# Funções

Funções tem o seguinte modelo:

Entradas -> Processamento -> Saídas

Go permite que uma função tenha mais de um retorno o que facilita bastante e torna o código mais limpo.

```
package main

import (
	"fmt"
)

func soma(x int, y int) int {
	return x + y
}

func swap(x string, y string) (string, string) {
	return y, x
}

// função que recebe uma função como parametro
func printFunc(f func(string) string, valor string) {
	aux := f(valor)
	fmt.Printf(aux)
}

func main() {
	fmt.Printf("Funções!\r\n")

	// função anonima que vamos passar para printFunc
	f := func(v string) string {
		return "Olá " + v + "!\r\n"
	}

	fmt.Printf("Soma 1+1 = %v\r\n", soma(1, 1))

	r1, r2 := swap("A", "B")
	fmt.Printf("troca 1, 2 = %v, %v\r\n", r1, r2)

	printFunc(f, "Cesar")

}
```

---
[Inicio](README.md) | [Variáveis <-](variaveis.md)