<div align="justify">

# 📌 Desafio Técnico - Planejamento e Casos de Teste

## 🎯 Objetivo
O presente projeto tem como finalidade evidenciar minhas competências técnicas e analíticas, por meio do planejamento estruturado e da documentação detalhada de cenários de teste, assegurando clareza, organização e qualidade.

## 🚀 Jornada do Usuário
Aplicativo: <b>Americanas</b>

Fluxo escolhido: <b>Login → Seleção de Produto → Adição ao Cesto</b>

<p>O usuário acessa o aplicativo, realiza login com credenciais válidas (e-mail e senha), navega para a tela inicial, pesquisa um determinado produto pela caixa de busca, seleciona o item e o adiciona ao cesto de compras.</p>

<p>Esse fluxo é essencial para o negócio, pois representa o caminho crítico até a conversão.</p>

## 🧪 Resumo dos Casos de Teste

<table>
  <tr>
    <th>Código</th>
    <th>Caso de Teste</th>
    <th>Resultado Esperado</th>
    <th>Tipo</th>
  </tr>
  <tr>
    <td><a href="#ct01">CT01</a></td>
    <td>Login com credenciais válidas</td>
    <td>Usuário autenticado</td>
    <td>🟢 Sucesso</td>
  </tr>
  <tr>
    <td><a href="#ct02">CT02</a></td>
    <td>Login com credenciais inválidas</td>
    <td>Mensagem de erro exibida</td>
    <td>🔴 Falha</td>
  </tr>
  <tr>
    <td><a href="#ct03">CT03</a></td>
    <td>Selecionar um produto</td>
    <td>Tela de detalhes exibida</td>
    <td>🟢 Sucesso</td>
  </tr>
  <tr>
    <td><a href="#ct04">CT04</a></td>
    <td>Adicionar produto ao cesto</td>
    <td>Produto adicionado ao cesto</td>
    <td>🟢 Sucesso</td>
  </tr>
  <tr>
    <td><a href="#ct05">CT05</a></td>
    <td>Adicionar mesmo produto mais de uma vez</td>
    <td>Quantidade incrementada (+1)</td>
    <td>🟢 Sucesso</td>
  </tr>
</table>

---

## 🖥️ Pré-requisitos do Ambiente

| Requisito | Detalhes / Valor esperado |
|-----------|--------------------------|
| Sistema Operacional (host) |	Windows 10/11, macOS ou Linux |
| Android (emulador/dispositivo) | Versão 16 ou superior |
| Dispositivo |	Smartphone físico ou emulador compatível |
| App em teste | `com.b2w.americanas` (versão 12.48.0 ou superior) |
| Permissões do app | Todas concedidas para evitar bloqueios em testes automatizados |
| Ferramenta de automação | Maestro.dev versão 2.0 ou superior |

---

## ⚙️ Variáveis de Ambiente

Para executar os testes automatizados no aplicativo das Americanas, utilizei algumas variáveis de ambiente, garantindo flexibilidade e segurança:

| Variável | Descrição | Exemplo |
|----------|-----------|---------|
| `APP_ID` | Identificador do aplicativo | com.b2w.americanas |
| `EMAIL` | E-mail de teste do usuário | testes.kobe.gbrancher@gmail.com |
| `PASSWORD` | Senha de teste do usuário | DesafioKobe@2025 |

**Observações:**  
- As variáveis de ambiente podem ser definidas em um arquivo .env ou na IDE do Maestro Studio.

![Desktop - Maestro Studio - Desktop - 28 August 2025](https://github.com/user-attachments/assets/3a3aac62-596e-4fe9-8a5d-3c94eeb2736b)
Definindo variáveis de ambiente no Maestro Studio.

---

## 🔍 Detalhes dos Casos de Teste

### <div id="ct01">📝 CT01: Login com credenciais válidas</div>
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

### <div id="ct02">📝 CT02: Login com credenciais inválidas</div>
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

### <div id="ct03">📝 CT03: Selecionar um produto</div>
- **Pré-condição:** O usuário está logado.
- **Passos:**
  - Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  - Clicar no botão "enter" do teclado.
  - Selecionar o produto buscado.
- **Resultado Esperado:** A tela de detalhes do produto será exibida.

---

### <div id="ct04">📝 CT04: Adicionar produto ao cesto</div>
- **Pré-condição:** O usuário está logado.
- **Passos:**
  - Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  - Clicar no botão "enter" do teclado.
  - Selecionar o produto buscado.
  - Clicar no botão "comprar".
  - Clicar no botão "adicionar e ir para a cesta".
- **Resultado Esperado:** A tela Cesta será exibida com o produto `HQS60NKHM` adicionado.

---

### <div id="ct05">📝 CT05: Adicionar mesmo produto mais de uma vez</div>
- **Pré-condição:** O usuário está logado e o produto já está no cesto.
- **Passos:**
  - Na tela Home, informar no campo de busca: `HQS60NKHM` (modelo de smart tv).
  - Clicar no botão "enter" do teclado.
  - Selecionar o produto buscado.
  - Clicar no botão "comprar".
  - Clicar novamente no botão "adicionar e ir para a cesta".
- **Resultado Esperado:** O produto `HQS60NKHM` aparecerá no cesto com a quantidade incrementada (+1).

</div>
