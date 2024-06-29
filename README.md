# Vue 3 + Pinia Todo List App

![Vue.js](https://img.shields.io/badge/vuejs-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D)
![Pinia](https://img.shields.io/badge/pinia-%23ffd859.svg?style=for-the-badge&logo=vuedotjs&logoColor=black)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![PNPM](https://img.shields.io/badge/pnpm-%234a4a4a.svg?style=for-the-badge&logo=pnpm&logoColor=f69220)

Uma aplicação de gerenciamento de tarefas desenvolvida com Vue.js 3, Pinia e TypeScript. Este projeto demonstra boas práticas de desenvolvimento front-end, incluindo gerenciamento de estado eficiente e componentes reutilizáveis.

## Demo

Veja a aplicação em ação: [Todo List App Demo](https://todolist-vue-pinia.netlify.app/)

## Funcionalidades

- Adicionar novas tarefas
- Marcar tarefas como concluídas
- Remover tarefas
- Feedback visual através de animações CSS
- Alerta de erro com barra de progresso para entradas inválidas

## Tecnologias Utilizadas

- Vue.js 3.4.29
- Pinia 2.1.7
- TypeScript 5.4.0
- Vite 5.3.1
- ESLint e Prettier para linting e formatação
- Vue DevTools para desenvolvimento
- pnpm para gerenciamento de pacotes

## Pré-requisitos

Certifique-se de ter o pnpm instalado em seu sistema. Se não tiver, você pode instalá-lo seguindo as instruções em [pnpm.io](https://pnpm.io/installation).

## Instalação e Execução Local

Para executar este projeto localmente, siga estes passos:

1. Clone o repositório:

git clone https://github.com/seu-usuario/vue-pinia-todo-list.git

2. Navegue até o diretório do projeto:

cd vue-pinia-todo-list

3. Instale as dependências:

pnpm install

4. Execute o servidor de desenvolvimento:

pnpm dev

5. Abra seu navegador e acesse `http://localhost:5173`

## Scripts Disponíveis

- `pnpm dev`: Inicia o servidor de desenvolvimento
- `pnpm build`: Compila e minifica para produção
- `pnpm preview`: Visualiza a versão de produção localmente
- `pnpm type-check`: Executa a verificação de tipos
- `pnpm lint`: Executa o linter
- `pnpm format`: Formata o código com Prettier

## Configuração do Projeto

Este projeto utiliza Vite como ferramenta de build. A configuração pode ser encontrada em `vite.config.ts`. Algumas características notáveis incluem:

- Uso do plugin `@vitejs/plugin-vue` para suporte ao Vue 3
- Configuração de alias para imports (`@` aponta para o diretório `src`)
- Uso do plugin `vite-plugin-vue-devtools` para melhorar a experiência de desenvolvimento
