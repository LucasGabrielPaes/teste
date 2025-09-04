```mermaid
classDiagram
  class instrumentos {
     -nome: string
    -preco: float
    +getPreco(): float
  }

  class Cordas {
   -nome: string
    -preco: float
    +getPreco(): float
}

 class Sopros {
   -nome: string
    -preco: float
    +getPreco(): float
}

 class Percussoes {
   -nome: string
    -preco: float
    +getPreco(): float
}

Pedido "1" --> "*" Produto : contém
  Pedido "*" --> "1" Cliente : feito por
```
