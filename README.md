## 🎵 Diagrama de Classes – Instrumentos Musicais

```mermaid
classDiagram
  class Produto {
    -id: int
    -nome: string
    -preco: float
    +getPreco(): float
    +exibirInfo(): string
  }

  class Instrumento {
    -marca: string
    +tocarDemo(): void
    +getMarca(): string
  }

  class Cordas {
    -tipoCordas: string
    +afinar(): void
    +getTipoCordas(): string
  }

  class Metais {
    -material: string
    +polir(): void
    +getMaterial(): string
  }

  class Percussao {
    -tipoPercussao: string
    +ritmar(): void
    +getTipoPercussao(): string
  }

  class Acessorio {
    -categoria: string
    +usar(): void
    +getCategoria(): string
  }

  %% Heranças
  Produto <|-- Instrumento
  Produto <|-- Acessorio
  Instrumento <|-- Cordas
  Instrumento <|-- Metais
  Instrumento <|-- Percussao
