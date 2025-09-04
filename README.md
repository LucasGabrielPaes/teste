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
    +getDescricao(): string
}

 class Sopros {
   -nome: string
    -preco: float
    +getPreco(): float
    +getDescricao(): string
}

 class Percussoes {
   -nome: string
    -preco: float
    +getPreco(): float
    +getDescricao(): string
}

instrumentos "1" --> "*" Cordas : contém
instrumentos "1" --> "*" Sopros : contém
instrumentos "1" --> "*" Percussoes : contém
```
