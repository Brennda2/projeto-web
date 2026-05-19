# 🛍️ Projeto Web - Catálogo de Produtos

## 📌 Sobre o projeto

Este projeto consiste em uma aplicação web desenvolvida com **Vue.js**, tendo o objetivo de apresentar um catálogo de produtos consumidos por uma API externa.

A aplicação permite visualizar produtos de forma dinâmica, exibindo informações como imagem, nome, categoria, preço e avaliação. Além disso, conta com sistema de paginação para navegação entre os itens.

---

## 🛠️ Tecnologias utilizadas

As seguintes tecnologias foram utilizadas no desenvolvimento:

- **Vue.js 3**
- **Vite**
- **Tailwind CSS**
- **Axios**
- **JavaScript**
- **HTML5**
- **CSS3**

---

## 📂 Estrutura do projeto

```bash
src/
│
├── assets/                # Imagens e arquivos estáticos
├── components/
│   ├── ProductCard.vue    # Card individual de produto
│   └── ProductList.vue    # Lista de produtos
│
├── composables/
│   └── useProducts.js     # Lógica de produtos e paginação
│
├── service/
│   └── productService.js  # Comunicação com API
│
├── App.vue
├── main.js
└── style.css
```

---


## ⚙️ Como executar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/projeto-web.git
```

### 2. Acesse a pasta

```bash
cd projeto-web
```

### 3. Instale as dependências

```bash
npm install
```

### 4. Execute o projeto

```bash
npm run dev
```

---
