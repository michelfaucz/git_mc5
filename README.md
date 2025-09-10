# 🧪 Testes de Login

Este projeto contém uma suíte de testes automatizados para validar o processo de login de usuários. Os testes garantem que o sistema de autenticação esteja funcionando corretamente, cobrindo casos positivos e negativos.

## ✅ Objetivos dos Testes

- Verificar se usuários válidos conseguem fazer login com sucesso.
- Garantir que usuários inválidos sejam bloqueados.
- Validar mensagens de erro apropriadas.
- Testar limites de campos (ex: senha muito curta).
- Verificar comportamento após múltiplas tentativas falhas.

## 🧰 Tecnologias Utilizadas

- [x] Node.js / Python / Java (dependendo do projeto)
- [x] Framework de testes: Jest / Pytest / JUnit
- [x] Ferramentas de automação: Selenium / Cypress / Playwright

## 📋 Casos de Teste

| Caso de Teste                         | Descrição                                                                 | Resultado Esperado         |
|--------------------------------------|---------------------------------------------------------------------------|----------------------------|
| Login com credenciais válidas        | Usuário insere e-mail e senha corretos                                    | Login bem-sucedido         |
| Login com senha incorreta            | Usuário insere e-mail correto e senha errada                              | Erro: "Senha inválida"     |
| Login com e-mail não cadastrado      | Usuário insere e-mail inexistente                                         | Erro: "Usuário não encontrado" |
| Campos vazios                        | Usuário tenta logar sem preencher os campos                               | Erro: "Preencha todos os campos" |
| Múltiplas tentativas falhas          | Usuário erra a senha várias vezes consecutivas                            | Conta bloqueada temporariamente |
| Login após logout                    | Usuário faz login, logout e tenta logar novamente                         | Login bem-sucedido         |

## 🔐 Considerações de Segurança

- As senhas nunca devem ser armazenadas em texto plano.
- O sistema deve implementar proteção contra ataques de força bruta.
- Tokens de sessão devem expirar após período de inatividade.

## 🚀 Como Executar os Testes

```bash
# Instalar dependências
npm install

# Executar testes
npm test
