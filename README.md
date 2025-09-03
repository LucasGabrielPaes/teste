## 🎵 Classes de Instrumentos Musicais

No sistema da loja de instrumentos musicais, os **Instrumentos** são um tipo especial de Produto.  
Eles se subdividem em três categorias principais: **Cordas**, **Metais** e **Percussão**.  
Além disso, existem também os **Acessórios**, que são produtos relacionados mas não são instrumentos diretamente (ex.: palhetas, baquetas, afinadores).

---

### Classe Produto
Base para todos os itens da loja.  
Representa qualquer mercadoria cadastrada no sistema.

**Atributos**
- `id : int` → Identificador único.  
- `nome : String` → Nome do produto.  
- `preco : float` → Valor unitário do produto.  

**Métodos**
- `getPreco() : float` → Retorna o preço do produto.  
- `exibirInfo() : String` → Retorna uma descrição formatada.  

---

### Classe Instrumento (herda de Produto)
Classe abstrata que representa qualquer instrumento musical.

**Atributos**
- `marca : String` → Marca do instrumento.  

**Métodos**
- `tocarDemo() : void` → Simula a execução do instrumento.  
- `getMarca() : String` → Retorna a marca.  

---

### Classe Cordas (herda de Instrumento)
Instrumentos que produzem som pela vibração de cordas.  
Exemplos: guitarra, violão, violino.

**Atributos**
- `tipoCordas : String` → Tipo de corda (aço, nylon, etc.).  

**Métodos**
- `afinar() : void` → Permite afinar o instrumento.  
- `getTipoCordas() : String` → Retorna o tipo de cordas.  

---

### Classe Metais (herda de Instrumento)
Instrumentos de sopro feitos de metal.  
Exemplos: trompete, trombone, saxofone.

**Atributos**
- `material : String` → Tipo de material (latão, bronze, etc.).  

**Métodos**
- `polir() : void` → Realiza manutenção no instrumento.  
- `getMaterial() : String` → Retorna o material.  

---

### Classe Percussão (herda de Instrumento)
Instrumentos que produzem som por impacto ou fricção.  
Exemplos: bateria, tambor, pandeiro.

**Atributos**
- `tipoPercussao : String` → Classificação (membranofone, idiofone, etc.).  

**Métodos**
- `ritmar() : void` → Executa um ritmo básico.  
- `getTipoPercussao() : String` → Retorna o tipo de percussão.  

---

### Classe Acessório (herda de Produto)
Produtos auxiliares ao uso dos instrumentos.  
Exemplos: palhetas, baquetas, capas, afinadores.

**Atributos**
- `categoria : String` → Categoria do acessório.  

**Métodos**
- `usar() : void` → Simula o uso do acessório.  
- `getCategoria() : String` → Retorna a categoria.  

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
