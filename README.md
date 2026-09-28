CRISTINA GABRIELY PINTO CAMPOS	Prova Paulista 10
Nota final do Bimestre  10

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# ATIVIDADE AVALIATIVA — MEU PERFIL EM REACT

*Nome:* Cristina Gabriely Pinto Campos
*Turma:* 3DS

## 1. Criar uma página com o título "Meu Perfil"

A página terá como título principal **“Meu Perfil”**.

```jsx
<h1>Meu Perfil</h1>
```

## 2. Exibir o nome do aluno e uma pequena apresentação

Meu nome é **Cristina**. Sou estudante de Desenvolvimento de Sistemas e estou aprendendo desenvolvimento Front-end e React.

```jsx
<h2>Meu nome é Cristina</h2>
<p>
  Sou estudante de Desenvolvimento de Sistemas e estou
  aprendendo desenvolvimento Front-end e React.
</p>
```

## 3. Inserir uma imagem ou avatar

Será utilizado um avatar para representar o perfil.

```jsx
<img src="/avatar.png" alt="Meu avatar" />
```

## 4. Criar pelo menos um componente próprio

Um componente chamado `Apresentacao` será criado para mostrar uma pequena apresentação.

```jsx
function Apresentacao() {
  return (
    <div>
      <h2>Olá!</h2>
      <p>
        Estou aprendendo React e desenvolvimento Front-end.
      </p>
    </div>
  );
}
```

A atividade pede a criação de pelo menos um componente próprio. 

## 5. Criar um botão com evento `onClick`

Será criado um botão chamado **“Conheça meu perfil”**. Quando o usuário clicar, uma função será executada.

```jsx
<button onClick={mostrarMensagem}>
  Conheça meu perfil
</button>
```

## 6. Utilizar `useState` para modificar uma informação

O `useState` será utilizado para alterar o título da página quando o botão for clicado.

```jsx
const [texto, setTexto] = useState("Meu Perfil");

function mostrarMensagem() {
  setTexto("Bem-vindo ao meu perfil!");
}
```

O `useState` permite armazenar uma informação que pode mudar durante o uso da página. Quando o estado muda, o React atualiza a interface. 

---

# 7. Código completo

### `App.jsx`

```jsx
import { useState } from "react";
import "./App.css";

// Componente próprio de apresentação
function Apresentacao() {
  return (
    <div className="apresentacao">
      <h2>Olá!</h2>

      <p>
        Sou estudante de Desenvolvimento de Sistemas
        e estou aprendendo desenvolvimento Front-end e React.
      </p>
    </div>
  );
}

function App() {
  // Estado utilizado para alterar o título
  const [texto, setTexto] = useState("Meu Perfil");

  // Função executada ao clicar no botão
  function mostrarMensagem() {
    setTexto("Bem-vindo ao meu perfil!");
  }

  return (
    <div className="perfil">

      <h1>{texto}</h1>

      <img
        src="/avatar.png"
        alt="Meu avatar"
        className="avatar"
      />

      <h2>Meu nome é Cristina</h2>

      <Apresentacao />

      <button onClick={mostrarMensagem}>
        Conheça meu perfil
      </button>

    </div>
  );
}

export default App;
```

### `App.css`

```css
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background-color: #f2f2f2;
}

.perfil {
  width: 400px;
  margin: 80px auto;
  padding: 30px;
  text-align: center;
  background-color: white;
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

.avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
}

.apresentacao {
  margin: 20px 0;
}

button {
  padding: 12px 20px;
  border: none;
  border-radius: 8px;
  background-color: #646cff;
  color: white;
  cursor: pointer;
}

button:hover {
  background-color: #4f55d8;
}
```

---

# 8. Desafio extra — Modo Escuro

Para criar o modo escuro, podemos utilizar o `useState` para armazenar se o modo escuro está ativado ou não.

```jsx
const [modoEscuro, setModoEscuro] = useState(false);
```

O botão pode alterar esse estado:

```jsx
<button onClick={() => setModoEscuro(!modoEscuro)}>
  Modo Escuro
</button>
```

Nesse caso, a informação armazenada no estado é **`true` ou `false`**, indicando se o modo escuro está ativado.

A atividade propõe justamente utilizar um estado para controlar essa mudança de aparência. 

---

# 9. Pergunta para reflexão

### O que o React facilitou na construção dessa interface em comparação com uma página feita apenas com HTML, CSS e JavaScript sem componentes?

**Resposta:**

O React facilitou a construção da interface porque permite dividir a página em componentes menores e reutilizáveis. Isso deixa o código mais organizado e facilita a criação de interações, como a alteração de informações utilizando o `useState`. 

---
