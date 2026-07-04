🏗️ Sistema de Gestão (Projeto Extensionista)

[![Next.js](https://img.shields.io/badge/Next.js-14%2B-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-18%2B-blue?style=for-the-badge&logo=react)](https://react.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Shadcn/ui](https://img.shields.io/badge/Shadcn%2Fui-UI_Components-black?style=for-the-badge)](https://ui.shadcn.com/)

Repositório Frontend desenvolvido como parte da disciplina de **Projeto Extensionista**. Este sistema web engloba uma série de interfaces (telas) de administração para gerenciar a logística, pessoas e recursos de um ecossistema integrado (como um canteiro de obras ou projeto agrícola).

---

## 🎯 Objetivo e Arquitetura do Projeto

O projeto foi desenhado focando em uma excelente **Experiência do Usuário (UX)** e em uma interface moderna. A aplicação está subdividida em múltiplos módulos focados em domínios de negócio específicos, que se comunicam via API REST.

**Módulos / Aplicações desenvolvidas:**
*   🔐 **Autenticação (Velocity4):** Tela principal de Login, Cadastro de Usuários e Dashboard com redirecionamento de rotas.
*   👷 **Cadastro de Trabalhadores:** Formulário avançado com validação de **CPF**, busca automática de endereço via **API ViaCEP** e alocação.
*   🏠 **Cadastro de Alojamentos:** CRUD e listagem com busca filtrada em tempo real para gerenciar moradias/repúblicas.
*   📦 **Cadastro de Materiais:** Controle de estoque utilizando campos numéricos validados e combobox (auto-complete) para locais de armazenamento.
*   🚜 **Cadastro de Veículos & Canteiro:** Módulos adicionais para a frota e gestão local.

---

## 🛠️ Stack Tecnológica e Boas Práticas

O frontend foi inteiramente construído com o que há de mais moderno no ecossistema React, garantindo tipagem estática, validação de dados no cliente e estilização consistente.

*   **Framework Core:** Next.js (App Router)
*   **Linguagem:** TypeScript
*   **Estilização:** Tailwind CSS + PostCSS
*   **Biblioteca de Componentes:** Shadcn/ui (Radix UI primitivos + Tailwind)
*   **Gerenciamento de Formulários:** `react-hook-form`
*   **Validação de Schemas:** `zod` (Integrado perfeitamente aos formulários)
*   **Notificações (Toasts):** `sonner`
*   **Ícones:** `lucide-react`

> **Destaque Técnico:** Todos os formulários possuem tratamentos de erros refinados (como bloqueio de quantidades negativas e CPFs inválidos), formatação em tempo real (máscaras) e feedback visual (Toasts) informando o status da requisição para a API back-end.

---

## 📋 Pré-requisitos

Para rodar os módulos localmente na sua máquina, você vai precisar de:

*   **Node.js** (Versão 18 ou superior)
*   Gerenciador de pacotes: `npm`, `yarn` ou `pnpm`
*   **Back-end em execução:** As aplicações frontend estão configuradas para fazer requisições para a porta `3300` (ex: `http://localhost:3300/funcionarios`). Garanta que sua API (JSON Server, Node, Java, etc) esteja ativa nesta porta.

---

## ⚙️ Como Executar o Projeto Localmente

Como a estrutura possui múltiplos diretórios contendo aplicações Next.js, você deve entrar no diretório do módulo que deseja testar.

### 1. Clonar o repositório
```bash
git clone [https://github.com/DanielScarparo/danielscarparo-telas-do-trabalho.git](https://github.com/DanielScarparo/danielscarparo-telas-do-trabalho.git)
2. Rodando o Módulo de Trabalhadores (Exemplo)
Bash
cd danielscarparo-telas-do-trabalho/cadastro-de-trabalhadores
````
# Instale as dependências
````
npm install
# ou pnpm install / yarn install
````
# Execute o servidor de desenvolvimento
npm run dev
A aplicação subirá localmente. Acesse: http://localhost:3000.

(Repita este passo para os demais diretórios como cadastro-materiais-main, cadastro-de-alojamentos-main ou para a raiz onde está o Login).
````
📂 Estrutura de Diretórios
O código-fonte de cada módulo segue o padrão limpo do Next.js App Router:

Plaintext
├── app/                  # Rotas da aplicação (Login, Register, Dashboard)
├── cadastro-de-trabalhadores/
│   ├── app/              # Páginas e layout (Next.js 14+)
│   ├── components/       # Componentes globais e do Shadcn UI
│   └── utils/            # Funções puras (cep-service.ts, cpf-validator.ts)
│
├── cadastro-materiais-main/
│   ├── actions/          # Server Actions para requisições
│   └── ...
│
├── cadastro-de-alojamentos-main/
└── components.json       # Arquivo de configuração do Shadcn UI
````
👤 Autor
Daniel Alves Scarparo Silva

Desenvolvido como parte do portfólio acadêmico e profissional em Engenharia/Desenvolvimento de Software.
