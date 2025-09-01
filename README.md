# Diagrama de Classes – Instrumentos

```mermaid
classDiagram
  class Produto {
    +getPreco(): float
    +getDescricao(): string
  }

  class Instrumento {
    +tocar(): void
    +afinar(): void
  }

  class Cordas {
    +trocarCordas(): void
    +getMaterialCordas(): string
  }

  class Metais {
    +limpar(): void
    +getTonalidade(): string
  }

  class Percussao {
    +bater(): void
    +getTipoPercussao(): string
  }

  Produto <|-- Instrumento
  Instrumento <|-- Cordas
  Instrumento <|-- Metais
  Instrumento <|-- Percussao
