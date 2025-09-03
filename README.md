# 🎵 Sistema de Loja de Instrumentos Musicais  

## 📌 Classe **Instrumento**  

A classe **Instrumento** representa os produtos da loja.  
Ela é **abstrata** e se especializa em três tipos principais: **Cordas**, **Percussão** e **Sopro**.  

---

### 🔹 Atributos
- **Instrumento** → `id`, `nome`, `preco`, `marca`, `estoque`  
- **Cordas** → `numCordas`, `tipoMadeira`  
- **Percussão** → `tipo`, `material`  
- **Sopro** → `afinacao`, `material`  

---

### 🔹 Métodos
- **Instrumento** → `calcularPrecoFinal()`, `verificarEstoque()`  
- **Cordas** → `substituirCorda()`, `afinar()`  
- **Percussão** → `trocarPele()`, `regularSom()`  
- **Sopro** → `limpar()`, `ajustarAfinacao()`  

---

## 📊 Diagrama UML – Instrumentos  

```mermaid
classDiagram
  class Instrumento {
    -id: int
    -nome: String
    -preco: double
    -marca: String
    -estoque: int
    +calcularPrecoFinal() double
    +verificarEstoque() boolean
  }

  class Cordas {
    -numCordas: int
    -tipoMadeira: String
    +substituirCorda(): void
    +afinar(): void
  }

  class Percussao {
    -tipo: String
    -material: String
    +trocarPele(): void
    +regularSom(): void
  }

  class Sopro {
    -afinacao: String
    -material: String
    +limpar(): void
    +ajustarAfinacao(): void
  }

  Instrumento <|-- Cordas
  Instrumento <|-- Percussao
  Instrumento <|-- Sopro

