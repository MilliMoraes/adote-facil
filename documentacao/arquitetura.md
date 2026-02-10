# Análise da Arquitetura de Software


## 1. Identificação da Arquitetura
O "Adote Fácil" possuí arquitetura **Cliente-Servidor** com separação entre as responsabilidades de interface e lógica de negócio:

* **Frontend (Cliente):** Desenvolvido com **Next.js e React**, focado na interface dinâmica e consumo da API.
* **Backend (Servidor):** Um **Monólito** construído em **Node.js e Express**, que gerencia rotas, autenticação e a lógica de persistência.

## 2. Justificativa
* **Desacoplamento:** A comunicação via API REST (utilizando Axios no frontend) permite que as duas partes do sistema sejam desenvolvidas e implantadas de forma independente.
* **Padronização de Dados:** O uso do **Prisma ORM** com **PostgreSQL** garante que a estrutura das tabelas (usuários, animais e chats) seja consistente e fácil de manter através de migrações.

## 3. Diagrama de Componentes
O fluxo de dados segue a seguinte estrutura:

[Navegador] > [Frontend (Next.js/React)] > [API (Express)] > [ORM (Prisma)] > [Banco de Dados (PostgreSQL)]

