<p align="center">
  <img src="img/img.jpg" alt="Transação API" width="600"/>
</p>

<h1 align="center">💳 Transação API</h1>

<p align="center">
  API REST desenvolvida para <strong>gerenciar transações financeiras</strong> e <strong>calcular estatísticas</strong> das transações realizadas nos últimos 60 segundos.<br>
  Construída com <strong>Java 21</strong> e <strong>Spring Boot</strong>, seguindo boas práticas de arquitetura e performance.
</p>

---

## 🚀 Tecnologias Utilizadas

- ☕ **Java 21+**
- 🌱 **Spring Boot**
- 🧱 **Maven**
- 🐳 **Docker** (opcional)
- 🧰 **Git**

---

## ⚙️ Pré-requisitos

Antes de iniciar, verifique se você possui instalado:

- `Java` (JDK 21 ou superior)
- `Maven` (3.8.1 ou superior)
- `Git`
- `Docker` (opcional)

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

🐳 Executar com Docker (Opcional)
4️⃣ Criar a Imagem Docker
bash
Copy code
docker build -t api-transacoes .
5️⃣ Executar o Container
bash
Copy code
docker run -p 8080:8080 api-transacoes
📘 Endpoints da API
➕ Criar Transação
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

📊 Consultar Estatísticas
GET /estatistica

Parâmetro	Tipo	Descrição
intervaloSegundos	integer	Opcional. Padrão: 60 segundos.

Exemplo de Resposta:

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
Este projeto foi desenvolvido como parte do Desafio Itaú Tech 2025, com foco em:

✅ Boas práticas de APIs REST

⚡ Processamento de dados em tempo real

📈 Cálculo de estatísticas de desempenho

👨‍💻 Autor
Desenvolvido por @Vitor2209
💼 Projeto do Desafio Itaú Tech 2025

<p align="center"> <sub>Feito com ❤️ e Java ☕</sub> </p> ```



