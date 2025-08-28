# acme-car-rental
Esta aplicação faz parte do livro Quarkus in action onde são desenvolvidos uma serie de microserviços que compõem uma aplicação de aluguel de carros 
---

## 🚗 Acme Car Rental – Monorepo Quarkus

Este repositório contém quatro projetos Quarkus que simulam uma aplicação de aluguel de carros. Cada projeto está isolado em sua própria pasta e pode ser executado independentemente.

---

### 📁 Estrutura do projeto

```
acme-car-rental/
├── inventory-cli/   # Aplicação cli para inserir veículos no inventory-service
├── inventory-service/   # API de inventário de veículos 
├── rental-service/   # API de aluguel
├── reservation-service/   # API de reservas
└── README.md
```

---

### 🛠️ Pré-requisitos

- [Java 17+](https://adoptium.net/)
- [Maven 3.8+](https://maven.apache.org/)
- [Quarkus CLI (opcional)](https://quarkus.io/guides/cli-tooling)
- Git

---

### 🚀 Como rodar os projetos

#### inventory-service 

```bash
cd inventory-service
./mvnw quarkus:dev
```
> Após rodar o projeto, a aplicação estara exposta no endereço:  http://localhost:8083

#### inventory-cli

```bash
cd inventory-cli
./mvnw clean package
```
> Após o build do você pode testar com o seguinte comando:
```bash
java -jar target/quarkus-app/quarkus-run.jar add KNIGHT Pontiac TransAM
```
> Quando executado, o cliente CLI se conecta ao serviço de inventário agindo como o servidor gRPC e insere um novo carro. O CLI log printa a seguinte mensagem confirmando que inseriu o carro:
```bash
 Inserted new car licensePlateNumber: "KNIGHT"
 manufacturer: "Pontiac"
 model: "TransAM"
```
---


---

### 🤝 Contribuições

Sinta-se à vontade para abrir issues ou pull requests. Este projeto é um laboratório de aprendizado com Quarkus — toda ajuda é bem-vinda!

---

