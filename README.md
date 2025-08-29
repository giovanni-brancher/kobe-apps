# 📌 Desafio Técnico - Planejamento e Casos de Teste

## 🎯 Objetivo
O presente projeto tem como finalidade evidenciar minhas competências técnicas e analíticas, por meio do planejamento estruturado e da documentação detalhada de cenários de teste, assegurando clareza, organização e qualidade.


## 🚀 Jornada do Usuário
Fluxo escolhido: **Login → Seleção de Produto → Adição ao Cesto**

**Descrição:**  
O usuário acessa o aplicativo, realiza login com credenciais válidas (e-mail e senha), navega para a tela inicial, pesquisa um determinado produto pela caixa de busca, seleciona o item e o adiciona ao cesto de compras.  
Esse fluxo é essencial para o negócio, pois representa o caminho crítico até a conversão.


## 🧪 Casos de Teste

## CT01: Login com credenciais válidas
- **Pré-condição:** O usuário já possui uma conta cadastrada.
- **Passos:**
  1. Abrir o app.
  2. Clicar no botão "Conta".
  3. Clicar no link "Entrar com e-mail".
  4. Clicar no botão "Entrar com e-mail e senha".
  5. Informar o e-mail válido: `testes.kobe.gbrancher@gmail.com`.
  6. Informar a senha válida: `DesafioKobe@2025`.
  7. Clicar em "Entrar".
- **Resultado Esperado:** O usuário será autenticado e redirecionado para a tela Perfil.

---

## CT02: Login com credenciais inválidas
- **Pré-condição:** O usuário digita uma senha incorreta.
- **Passos:**
  1. Abrir o app.
  2. Clicar no botão "Conta".
  3. Clicar no link "Entrar com e-mail".
  4. Clicar no botão "Entrar com e-mail e senha".
  5. Informar o e-mail válido: `testes.kobe.gbrancher@gmail.com`.
  6. Informar uma senha inválida: `SenhaErrada`.
  7. Clicar em "Entrar".
- **Resultado Esperado:** A mensagem `"Insira uma senha válida"` será exibida abaixo do campo "Senha" e o usuário permanecerá na tela de Login.

---

## CT03: Selecionar um produto
- **Pré-condição:** O usuário está logado.
- **Passos:**
  1. Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  2. Clicar no botão "enter" do teclado.
  3. Selecionar o produto buscado.
- **Resultado Esperado:** A tela de detalhes do produto será exibida.

---

## CT04: Adicionar produto ao cesto
- **Pré-condição:** O usuário está logado.
- **Passos:**
  1. Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  2. Clicar no botão "enter" do teclado.
  3. Selecionar o produto buscado.
  4. Clicar no botão "comprar".
  5. Clicar no botão "adicionar e ir para a cesta".
- **Resultado Esperado:** A tela Cesta será exibida com o produto `HQS60NKHM` adicionado.

---

## CT05: Adicionar mesmo produto mais de uma vez
- **Pré-condição:** O usuário está logado e o produto já está no cesto.
- **Passos:**
  1. Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  2. Clicar no botão "enter" do teclado.
  3. Selecionar o produto buscado.
  4. Clicar no botão "comprar".
  5. Clicar novamente em "adicionar e ir para a cesta".
- **Resultado Esperado:** O produto `HQS60NKHM` aparecerá no cesto com a quantidade incrementada (+1).
