classDiagram
  class Produto {
    +nome: string
    +preco: float
    +getPreco(): float
    +exibirInfo(): void
  }

  class Instrumento {
    +marca: string
    +modelo: string
    +tocar(): void
    +getMarca(): string
  }

  class Cordas {
    +numCordas: int
    +afinar(): void
    +getNumCordas(): int
  }

  class Metais {
    +tipoBocal: string
    +limpar(): void
    +getTipoBocal(): string
  }

  class Percussao {
    +tipoPele: string
    +bater(): void
    +getTipoPele(): string
  }

  Produto <|-- Instrumento
  Instrumento <|-- Cordas
  Instrumento <|-- Metais
  Instrumento <|-- Percussao
