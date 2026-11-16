# Banco VIO - Sistema de Conta Poupança
 
Sistema web para gerenciamento de uma conta poupança pessoal, desenvolvido como trabalho prático da disciplina de **Programação Web**. O usuário faz login, acessa sua conta e realiza depósitos e saques, com todos os dados persistidos em banco de dados MySQL.
 
## Integrantes
 
| Nome | Responsabilidade |
|------|------------------|
| Eduardo Erlacher Melo | Estruturamento e Programação |
| Estevão Nunes Agostini | Design e Banco de Dados |
| João Pedro Miranda Dossi | Design e Interatividade |
 
## Tecnologias utilizadas
 
| Camada | Tecnologia | Uso |
|--------|------------|-----|
| Frontend | **HTML5** | Estrutura das páginas |
| Frontend | **CSS3** | Estilização e layout responsivo |
| Frontend | **JavaScript** | Validações e interações no lado do cliente |
| Backend | **PHP** | Regras de negócio e comunicação com o banco |
| Banco de dados | **MySQL** | Armazenamento e gerenciamento dos dados |
| Design | **Figma** | Prototipação das telas |
 
## Funcionalidades
 
- Cadastro e login de usuários
- Cadastro, consulta, edição e exclusão (CRUD) das entidades do sistema, com confirmação antes de excluir
- Depósitos e saques na conta poupança
- Consulta de saldo e histórico de movimentações
- Registro de acessos (data e IP de cada login)
- Validação de dados no cliente (JavaScript) e no servidor (PHP)
## Protótipo no Figma
 
O protótipo das telas do sistema pode ser acessado pelo link abaixo:
 
[Ver protótipo no Figma](https://www.figma.com/design/NszAZKUkughuH9Vk0ZbLD5/Banco-VIO?node-id=0-1&p=f&t=EtAQwBi7mWlfCtPs-0)
 
## Modelagem de dados
 
Modelo Entidade-Relacionamento (MER) do banco de dados:
 
![Modelagem de dados do sistema de poupança](docs/modelagem-de-dados.png)
 
 
> Ajuste a estrutura conforme a organização real do seu projeto.
 
## Como executar
 
### Pré-requisitos
 
- [XAMPP](https://www.apachefriends.org/) (ou WAMP/Laragon) com **Apache**, **PHP** e **MySQL**
### Passo a passo
 
1. **Clone o repositório** dentro da pasta `htdocs` do XAMPP:
```bash
git clone URL_DO_REPOSITORIO
```
2. **Inicie** o Apache e o MySQL pelo painel do XAMPP.
3. **Crie o banco de dados:** acesse `http://localhost/phpmyadmin`, vá em **Importar** e selecione o arquivo `database/poupanca.sql`.
4. **Configure a conexão** em `config/conexao.php`:
```php
$host = "localhost";
$usuario = "root";
$senha = "";
$banco = "poupanca";
```
5. **Acesse o sistema** em `http://localhost/poupanca`.
### Usuário de demonstração
 
| E-mail | Senha |
|--------|-------|
| _preencher_ | _preencher_ |
 
## Regras de negócio
 
- Cada usuário possui uma única conta poupança.
- O saque não pode ser maior que o saldo disponível.
- Depósitos e saques devem ter valor maior que zero.
- Toda movimentação atualiza o saldo e fica registrada no histórico.
- Todo login é registrado com data e IP.
## Licença
 
Projeto desenvolvido para fins de acadêmicos.
 
