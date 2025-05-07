# 🚗 API de Estacionamento com Laravel + Docker

Este projeto é uma API desenvolvida com Laravel, destinada a permitir que usuários cadastrados realizem check-in e check-out em estacionamentos parceiros. Todo o ambiente é containerizado usando Docker e Docker Compose.

---

## 🔧 Como subir o projeto com Docker

> Certifique-se de ter o **Docker** e **Docker Compose** instalados na sua máquina.

### 1. Clone o repositório

```bash
git clone [https://github.com/marcos-26/estacionamento]
cd seu-repo/estacionamento

docker-compose up -d --build

### 2. A API estará disponível em:

http://localhost:8000

📡 Rotas da API
🧑‍💼 Autenticação de Usuário
Método	Endpoint	Descrição
POST	/register	Cadastra um novo usuário
POST	/login	Autentica o usuário (gera token)
POST	/logout	Desloga e invalida o token

👤 Gestão de Usuários (Requer autenticação via Sanctum)
Método	Endpoint	Descrição
GET	/users	Lista todos os usuários
GET	/users/{id}	Mostra detalhes de um usuário
PUT	/users/{id}	Atualiza um usuário
DELETE	/users/{id}	Remove um usuário
POST	/users/save-facial-biometrics	Salva biometria facial

🚘 Check-in/Check-out
Método	Endpoint	Descrição
POST	/checkin	Realiza check-in
POST	/checkout	Realiza check-out

🏠 Endereços
Método	Endpoint	Descrição
GET	/endereco/list	Lista todos os endereços
POST	/endereco/create	Cria um novo endereço
GET	/endereco/show{id}	Exibe um endereço
PUT	/endereco/update{id}	Atualiza um endereço
DELETE	/endereco/delete{id}	Deleta um endereço

🚗 Carros
Método	Endpoint	Descrição
POST	/car/create	Cadastra um carro
GET	/car/list	Lista todos os carros
GET	/car/show{id}	Mostra um carro
PUT	/car/update{id}	Atualiza um carro
DELETE	/car/delete{id}	Deleta um carro

🅿️ Estacionamentos
Método	Endpoint	Descrição
GET	/estacionamentos/list	Lista todos os estacionamentos
POST	/estacionamentos/create	Cadastra um novo estacionamento
GET	/estacionamentos/show{id}	Detalhes de um estacionamento
PUT	/estacionamentos/update{id}	Atualiza estacionamento
DELETE	/estacionamentos/delete{id}	Deleta estacionamento
POST	/estacionamentos/listvagas	Lista vagas disponíveis

💳 Pagamentos
Método	Endpoint	Descrição
POST	/pagamento/realizarpagamento	Cliente realiza pagamento
POST	/pagamento/receberpagamento	Estacionamento recebe pagamento

✅ Requisitos para rodar o projeto
Docker

Docker Compose

PHP 8.2+

Laravel 10+

MongoDB
