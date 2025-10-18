# 💳 Transação API

API REST desenvolvida para **gerenciar transações financeiras** e **calcular estatísticas** das transações realizadas nos últimos 60 segundos.  
O projeto foi construído com **Java 21** e **Spring Boot**, seguindo boas práticas de arquitetura e performance.

---

## 🚀 Tecnologias Utilizadas

- **Java 21+**
- **Spring Boot**
- **Maven**
- **Docker** (opcional)
- **Git**

---

## ⚙️ Variáveis de Ambiente

Para executar o projeto localmente, é necessário ter instalado:

- `Java` (JDK 21 ou superior)
- `Maven` (versão 3.8.1 ou superior)
- `Git`
- `Docker` (opcional, para execução em container)

---

## 🧩 Como Configurar o Projeto

### 1️⃣ Clonar o Repositório

```bash
git clone https://github.com/seu-usuario/api-transacoes.git
cd api-transacoes
2️⃣ Compilar o Projeto
bash
Copy code
mvn clean install
3️⃣ Executar o Projeto
bash
Copy code
mvn spring-boot:run
O servidor será iniciado em:
👉 http://localhost:8080

🐳 Como Rodar com Docker (Opcional)
4.1 Criar a Imagem Docker
Certifique-se de que o Docker está instalado e execute:

bash
Copy code
docker build -t api-transacoes .
4.2 Executar o Container
bash
Copy code
docker run -p 8080:8080 api-transacoes
📘 Documentação da API
➕ Receber Transações
POST /transacao

Parâmetro	Tipo	Descrição
valor	BigDecimal	Obrigatório. Valor da transação.
dataHora	OffsetDateTime	Obrigatório. Horário em que a transação ocorreu.

Exemplo de Requisição:

json
Copy code
{
  "valor": 120.50,
  "dataHora": "2025-10-18T14:32:00Z"
}
❌ Limpar Transações
DELETE /transacao

Remove todas as transações armazenadas.

📊 Calcular Estatísticas
GET /estatistica

Parâmetro	Tipo	Descrição
intervaloSegundos	integer	Opcional. Padrão: 60 segundos.

Resposta de Exemplo:

json
Copy code
{
  "soma": 450.75,
  "media": 150.25,
  "maximo": 200.00,
  "minimo": 100.50,
  "quantidade": 3
}
🧠 Sobre o Projeto
Este projeto foi desenvolvido como parte do Desafio Itaú Tech 2025, com foco em boas práticas de APIs REST, tratamento de dados em tempo real e estatísticas de desempenho.

👨‍💻 Autor
Desenvolvido por @Vitor2209
💼 Projeto do Desafio Itaú Tech 2025





