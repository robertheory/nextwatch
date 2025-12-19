# Resumo Oficial — Requisitos do Projeto Final (MVP)

## 1. Objetivo Geral

Desenvolver um sistema web componentizado onde diferentes módulos atuem como serviços autônomos, comunicando-se via REST e/ou GraphQL, aplicando os conceitos de componentização e serviços.

## 2. Arquitetura Obrigatória

- O sistema deve possuir, no mínimo, 3 módulos/componentes que se comunicam.
- Pelo menos um dos módulos deve ser externo (uma API pública externa, ex.: ViaCEP, FakeStore).
- A comunicação entre módulos deve ser via REST e/ou GraphQL.
- Cada módulo deve ser autônomo e cumprir uma função específica.

## 3. Persistência de Dados

O sistema deve possuir persistência de dados. Bancos permitidos:

- SQLite
- MySQL
- PostgreSQL

## 4. Repositórios e Organização

- Cada módulo deve ter seu próprio repositório público no GitHub.
- O código deve ser organizado com:
  - Estrutura de pastas clara
  - Nomes seguindo boas práticas (ex.: CamelCase, snake_case conforme a linguagem)
- Se usar exemplos vistos em aula, pelo menos 50% do código deve ser novo (caso contrário há penalização).

## 5. Docker (Obrigatório)

- Cada componente deve possuir um `Dockerfile` na raiz do repositório.
- O `Dockerfile` deve permitir a execução correta do componente via container.
- Penalizações:
  - `Dockerfile` ausente ou não funcional → –1,0 ponto (Interface/API principal)
  - `Dockerfile` ausente ou não funcional → –0,5 ponto (API secundária)
- Se utilizar `docker-compose`, o arquivo deve ficar na raiz do repositório da Interface ou da API principal.

## 6. Interface OU API Principal (5,0 pontos)

### Se for uma API

- Implementar uma API REST em Python (Flask ou FastAPI).
- Deve possuir no mínimo 4 rotas obrigatórias:
  1.  `GET`
  2.  `POST`
  3.  `PUT`
  4.  `DELETE`
- Ausência de qualquer método implica em –0,5 ponto.

### Se for uma Interface

- Desenvolver interface com HTML, CSS e JavaScript (frameworks como React/Next/Vue são permitidos).
- A interface deve consumir pelo menos 4 rotas HTTP distintas: `GET`, `POST`, `PUT`, `DELETE`.
- Ausência de qualquer método implica em –0,5 ponto.

## 7. Criatividade e Inovação (1,0 ponto)

- O domínio do sistema não pode ser igual aos exemplos apresentados em aula.
- Para APIs: adicionar funcionalidades além do CRUD básico (ex.: filtros, ordenação, paginação, autenticação).
- Para interfaces: propor interações ou visualizações diferenciadas (dashboards, gráficos, feedback visual, bibliotecas de componentes, etc.).

## 8. API Secundária / Backend Secundário (3,0 pontos)

- Implementar uma API REST ou GraphQL com no mínimo 4 rotas.
- Deve conter README com descrição e instruções de execução e um `Dockerfile` funcional.

## 9. API Externa (1,0 ponto)

- Utilizar uma API externa pública e gratuita.
- Documentar a API externa no `README` com:
  - Nome
  - Licença (se houver)
  - Necessidade de cadastro (se houver)
  - Rotas utilizadas
- É obrigatório consumir e tratar os dados da API externa (sem redirecionamento para outro site).

## 10. Documentação (README)

Cada componente deve conter um `README` com:

- Título e descrição do projeto
- Instruções completas de instalação e execução
- Uso de formatação clara (títulos, listas)
- Imagem/fluxograma da arquitetura

## 11. Entrega em Vídeo (Obrigatório)

- Vídeo de até 6 minutos.
- Seguir o roteiro obrigatório:
  1.  Objetivo da aplicação
  2.  Arquitetura e comunicação
  3.  API externa
  4.  Segunda componente (execução via Docker)
  5.  Componente principal (execução via Docker)
- Penalizações:
  - Estourar tempo → –0,5 ponto
  - Não cumprir roteiro → até –2,0 pontos
  - Não entregar vídeo → –2,0 pontos

## 12. Entrega Final

- Fornecer links públicos para:
  - Vídeo
  - Repositórios GitHub de cada componente (devem ser públicos)

---

Se quiser, eu posso:

- Gerar um checklist de arquivos obrigatórios por repositório (ex.: `Dockerfile`, `README.md`, rotas obrigatórias).
- Criar templates de `README` e `Dockerfile` para cada componente.
