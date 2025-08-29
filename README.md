# 📌 Desafio Técnico - Planejamento e Casos de Teste

## 🎯 Objetivo
<div align="justify">O presente projeto tem como finalidade evidenciar minhas competências técnicas e analíticas, por meio do planejamento estruturado e da documentação detalhada de cenários de teste, assegurando clareza, organização e qualidade.</div>

## 🚀 Jornada do Usuário
Fluxo escolhido: **Login → Seleção de Produto → Adição ao Cesto**

**Descrição:** 
<div align="justify">O usuário acessa o aplicativo, realiza login com credenciais válidas (e-mail e senha), navega para a tela inicial, pesquisa um determinado produto pela caixa de busca, seleciona o item e o adiciona ao cesto de compras.</div>

Esse fluxo é essencial para o negócio, pois representa o caminho crítico até a conversão.

## 🧪 Casos de Teste

### Resumo Visual dos Cenários de Teste

| Código | Cenário | Resultado Esperado | Tipo |
|--------|---------|------------------|------|
| [CT01](#ct01-login-com-credenciais-validas) | Login com credenciais válidas | Usuário autenticado e redirecionado para a tela Perfil | 🟢 Positivo |
| [CT02](#ct02-login-com-credenciais-inválidas) | Login com credenciais inválidas | Mensagem de erro exibida e usuário permanece na tela de Login | 🔴 Negativo |
| [CT03](#ct03-selecionar-um-produto) | Selecionar um produto | Tela de detalhes do produto exibida | 🟢 Positivo |
| [CT04](#ct04-adicionar-produto-ao-cesto) | Adicionar produto ao cesto | Produto adicionado ao cesto e exibido na tela Cesta | 🟢 Positivo |
| [CT05](#ct05-adicionar-mesmo-produto-mais-de-uma-vez) | Adicionar mesmo produto mais de uma vez | Produto no cesto com quantidade incrementada (+1) | 🟢 Positivo |

---

### CT01: Login com credenciais válidas
- **Pré-condição:** O usuário já possui uma conta cadastrada.
- **Passos:**
  - Abrir o app.
  - Clicar no botão "Conta".
  - Clicar no link "Entrar com e-mail".
  - Clicar no botão "Entrar com e-mail e senha".
  - Informar o e-mail válido: `testes.kobe.gbrancher@gmail.com`.
  - Informar a senha válida: `DesafioKobe@2025`.
  - Clicar em "Entrar".
- **Resultado Esperado:** O usuário será autenticado e redirecionado para a tela Perfil.

---

### CT02: Login com credenciais inválidas
- **Pré-condição:** O usuário digita uma senha incorreta.
- **Passos:**
  - Abrir o app.
  - Clicar no botão "Conta".
  - Clicar no link "Entrar com e-mail".
  - Clicar no botão "Entrar com e-mail e senha".
  - Informar o e-mail válido: `testes.kobe.gbrancher@gmail.com`.
  - Informar uma senha inválida: `SenhaErrada`.
  - Clicar em "Entrar".
- **Resultado Esperado:** A mensagem `"Insira uma senha válida"` será exibida abaixo do campo "Senha" e o usuário permanecerá na tela de Login.

---

### CT03: Selecionar um produto
- **Pré-condição:** O usuário está logado.
- **Passos:**
  - Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  - Clicar no botão "enter" do teclado.
  - Selecionar o produto buscado.
- **Resultado Esperado:** A tela de detalhes do produto será exibida.

---

### CT04: Adicionar produto ao cesto
- **Pré-condição:** O usuário está logado.
- **Passos:**
  - Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  - Clicar no botão "enter" do teclado.
  - Selecionar o produto buscado.
  - Clicar no botão "comprar".
  - Clicar no botão "adicionar e ir para a cesta".
- **Resultado Esperado:** A tela Cesta será exibida com o produto `HQS60NKHM` adicionado.

---

### CT05: Adicionar mesmo produto mais de uma vez
- **Pré-condição:** O usuário está logado e o produto já está no cesto.
- **Passos:**
  - Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  - Clicar no botão "enter" do teclado.
  - Selecionar o produto buscado.
  - Clicar no botão "comprar".
  - Clicar novamente no botão "adicionar e ir para a cesta".
- **Resultado Esperado:** O produto `HQS60NKHM` aparecerá no cesto com a quantidade incrementada (+1).
