# Documento de entrega

## Desenvolvimento de Operações Ágeis - DevOps

### Requisitos mínimos

| ID | Requisito | Onde foi coberto |
| --- | --- | --- |
| DEVOPS-M1 | Aplicar Code Review e Pull Requests com aprovações. | [PR #35 - revisão solicitando alterações](https://github.com/Argos-app/argos-backend-service/pull/35) e [aprovação posterior](https://github.com/Argos-app/argos-backend-service/pull/35); [PR #11 aprovada](https://github.com/Argos-app/argos-frontend-service/pull/11#pullrequestreview-5706413886). |
| DEVOPS-M2 | Utilizar cloud como infraestrutura de hospedagem. | [Acessos do frontend na Vercel][f-readme]; [workflow de publicação do backend na Discloud][b-deploy]. |
| DEVOPS-M3 | Utilizar tecnologia de container e orquestração, como Docker e Kubernetes. | [Dockerfile][b-docker]; [Deployment Kubernetes][b-k8s]; [roteiro de execução local][b-k8s-doc].

### Requisitos extras

| ID | Requisito | Onde foi coberto |
| --- | --- | --- |
| DEVOPS-E1 | Criar README completo do projeto. | [README do frontend][f-readme] e [guia de contribuição do backend][b-contrib]. |
| DEVOPS-E2 | Definir template de Pull Request e aplicá-lo durante o desenvolvimento. | [Template do backend][b-template]; [template do frontend][f-template]; [PR #35](https://github.com/Argos-app/argos-frontend-service/pull/35). |
| DEVOPS-E3 | Elaborar pipeline para implantação, como GitHub Actions ou Jenkins. | [Workflow de deploy do backend][b-deploy]; [workflow de CI com testes][b-ci]; [deploy do frontend][f-deploy]. |

## Desenvolvimento de Aplicações Dinâmicas

Os itens abaixo agrupam os principais critérios da disciplina.

### Requisitos mínimos

| ID | Requisito | Onde foi coberto |
| --- | --- | --- |
| DIN-M1 | Construir a aplicação com Vite, React e TypeScript, organizando componentes, páginas e tipos. | [Dependências e scripts][din-package]; [componentes][din-components]; [páginas][din-pages]; [tipos de domínio][din-types]. |
| DIN-M2 | Consumir a API por serviços tipados, tratar erros e configurar endereços por variáveis de ambiente. | [Service de usuários][din-service]; [tratamento de requisições][din-request]; [configuração de ambiente][din-env]. |
| DIN-M3 | Gerenciar estado e efeitos; renderizar listas com identificadores estáveis e apresentar carregamento e erros. | [Estado, efeitos e cancelamento na paginação][din-pagination]; [tabela e chave das linhas][din-table]; [testes de consultas][din-queries-test]. |
| DIN-M4 | Implementar navegação com React Router, parâmetros tratados e página para rotas inexistentes. | [Rotas e página curinga][din-app]; [validação do parâmetro de página][din-users]; [página não encontrada][din-notfound]. |
| DIN-M5 | Proporcionar formulários e navegação acessíveis, incluindo nomes, foco, contraste e mensagens de erro. | [Campo de entrada][din-input]; [formulário de usuários][din-form]; [testes de acessibilidade][din-access-test] e [contraste][din-contrast-test]. |
| DIN-M6 | Publicar a aplicação e manter histórico de desenvolvimento com commits identificáveis. | [Acessos publicados no README][din-readme]; [histórico da branch develop](https://github.com/Argos-app/argos-frontend-service/commits/develop/). |

### Requisitos extras

| ID | Requisito | Onde foi coberto |
| --- | --- | --- |
| DIN-E1 | Compartilhar autenticação com Context API e proteger rotas privadas. | [Provider e hook de autenticação][din-context]; [componente de rota privada][din-private]; [testes de autenticação][din-auth-test]. |
| DIN-E2 | Utilizar hooks tipados, reducer, cancelamento de requisições e carregamento sob demanda. | [Hook de paginação com reducer e AbortController][din-pagination]; [React.lazy e Suspense nas rotas][din-app]. |
| DIN-E3 | Salvar preferências em localStorage com versão e descarte seguro de dados incompatíveis. | [Leitura e gravação das preferências][din-preferences]; [testes das preferências][din-preferences-test]. |
| DIN-E4 | Validar e normalizar dados de formulários antes do envio. | [Validação tipada de usuários e propriedades][din-validation]; [validação antes das operações de usuários][din-mutations]; [testes de validação][din-validation-test]. |

[din-package]: https://github.com/Argos-app/argos-frontend-service/blob/develop/package.json
[din-components]: https://github.com/Argos-app/argos-frontend-service/tree/develop/src/components
[din-pages]: https://github.com/Argos-app/argos-frontend-service/tree/develop/src/pages
[din-types]: https://github.com/Argos-app/argos-frontend-service/tree/develop/src/types
[din-service]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/services/userService.ts
[din-request]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/services/serviceRequest.ts
[din-env]: https://github.com/Argos-app/argos-frontend-service/blob/develop/.env.example
[din-pagination]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/hooks/usePaginatedResource.ts
[din-table]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/components/Table/DataTable/DataTableComponent.tsx
[din-queries-test]: https://github.com/Argos-app/argos-frontend-service/blob/develop/tests/queries.integration.test.tsx
[din-app]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/App.tsx
[din-users]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/hooks/useUsers.ts
[din-notfound]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/pages/notFound/index.tsx
[din-input]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/components/Input/InputComponent.tsx
[din-form]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/components/CreateUserDrawer/CreateUserDrawerComponent.tsx
[din-access-test]: https://github.com/Argos-app/argos-frontend-service/blob/develop/tests/accessibility.integration.test.tsx
[din-contrast-test]: https://github.com/Argos-app/argos-frontend-service/blob/develop/tests/contrast.integration.test.tsx
[din-readme]: https://github.com/Argos-app/argos-frontend-service/blob/develop/README.md
[din-context]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/context/AuthContext.tsx
[din-private]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/components/PrivateRoute/PrivateRouteComponent.tsx
[din-auth-test]: https://github.com/Argos-app/argos-frontend-service/blob/develop/tests/auth.integration.test.tsx
[din-preferences]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/lib/interfacePreferences.ts
[din-preferences-test]: https://github.com/Argos-app/argos-frontend-service/blob/develop/tests/interfacePreferences.unit.test.ts
[din-validation]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/utils/validation.ts
[din-mutations]: https://github.com/Argos-app/argos-frontend-service/blob/develop/src/hooks/useUserManagement.ts
[din-validation-test]: https://github.com/Argos-app/argos-frontend-service/blob/develop/tests/validation.unit.test.ts

[f-readme]: https://github.com/Argos-app/argos-frontend-service/blob/8d994de7418c354d0dfbab7e1114079a5fe108b7/README.md#L1-L90
[f-template]: https://github.com/Argos-app/argos-frontend-service/blob/8d994de7418c354d0dfbab7e1114079a5fe108b7/.github/pull_request_template.md#L1-L33
[f-deploy]: https://github.com/Argos-app/argos-frontend-service/blob/8d994de7418c354d0dfbab7e1114079a5fe108b7/.github/workflows/deploy.yml#L1-L25
[b-deploy]: https://github.com/Argos-app/argos-backend-service/blob/5c17c651bb762f1eb5d3d9f8911ad992d452d4dd/.github/workflows/deploy.yml#L1-L59
[b-ci]: https://github.com/Argos-app/argos-backend-service/blob/5c17c651bb762f1eb5d3d9f8911ad992d452d4dd/.github/workflows/ci.yml#L1-L48
[b-docker]: https://github.com/Argos-app/argos-backend-service/blob/5c17c651bb762f1eb5d3d9f8911ad992d452d4dd/Dockerfile#L1-L21
[b-k8s]: https://github.com/Argos-app/argos-backend-service/blob/5c17c651bb762f1eb5d3d9f8911ad992d452d4dd/kubernetes/base/deployment.yaml#L1-L59
[b-k8s-doc]: https://github.com/Argos-app/argos-backend-service/blob/5c17c651bb762f1eb5d3d9f8911ad992d452d4dd/kubernetes/README.md#L1-L73
[b-contrib]: https://github.com/Argos-app/argos-backend-service/blob/5c17c651bb762f1eb5d3d9f8911ad992d452d4dd/CONTRIBUTING.md#L1-L174
[b-template]: https://github.com/Argos-app/argos-backend-service/blob/5c17c651bb762f1eb5d3d9f8911ad992d452d4dd/.github/pull_request_template.md#L1-L33
