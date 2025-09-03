## 🎵 Classes de Instrumentos Musicais

No sistema, os **Instrumentos** são um tipo de Produto e se dividem em **Cordas**, **Metais** e **Percussão**.  
Os **Acessórios** também são Produtos, mas não são instrumentos diretamente.

---

### Produto
- **Atributos**:  
  `id : int`, `nome : String`, `preco : float`  
- **Métodos**:  
  `getPreco() : float`, `exibirInfo() : String`

### Instrumento (herda de Produto)
- **Atributos**:  
  `marca : String`  
- **Métodos**:  
  `tocarDemo() : void`, `getMarca() : String`

### Cordas (herda de Instrumento)
- **Atributos**:  
  `tipoCordas : String`  
- **Métodos**:  
  `afinar() : void`, `getTipoCordas() : String`

### Metais (herda de Instrumento)
- **Atributos**:  
  `material : String`  
- **Métodos**:  
  `polir() : void`, `getMaterial() : String`

### Percussão (herda de Instrumento)
- **Atributos**:  
  `tipoPercussao : String`  
- **Métodos**:  
  `ritmar() : void`, `getTipoPercussao() : String`

### Acessório (herda de Produto)
- **Atributos**:  
  `categoria : String`  
- **Métodos**:  
  `usar() : void`, `getCategoria() : String`

---

### 🎼 Diagrama UML – Instrumentos

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

  Produto <|-- Instrumento
  Produto <|-- Acessorio
  Instrumento <|-- Cordas
  Instrumento <|-- Metais
  Instrumento <|-- Percussao

