# Aparatus

Aparatus é uma plataforma moderna para agendamento de serviços em barbearias, desenvolvida com foco em escalabilidade, experiência do usuário e facilidade de manutenção. Este projeto utiliza as melhores práticas do ecossistema React/Next.js, integra autenticação robusta e oferece uma interface fiel ao design do Figma.

## Tecnologias Utilizadas

- **Next.js 16 (App Router)**: Estrutura principal do frontend, com roteamento moderno e server components.
- **React 19**: Componentização, hooks e interatividade.
- **TypeScript**: Tipagem estática para maior segurança e produtividade.
- **Prisma ORM**: Modelagem e acesso eficiente ao banco de dados Postgres.
- **Postgres**: Banco de dados relacional robusto e escalável.
- **shadcn/ui**: Biblioteca de componentes UI acessíveis e customizáveis.
- **Tailwind CSS**: Estilização utilitária, usando apenas cores do tema definidas em `globals.css`.
- **BetterAuth**: Solução de autenticação segura e flexível.

## Estrutura do Projeto

```
├── app/
│   ├── _components/
│   │   ├── ui/           # Componentes reutilizáveis (Button, Calendar, Card, etc.)
│   │   ├── ...           # Componentes de domínio (service-item, barbershop-item, etc.)
│   ├── api/              # Rotas de API (auth, barbershops)
│   ├── generated/prisma/ # Tipos e cliente Prisma gerados
│   ├── globals.css       # Tema e variáveis CSS
│   ├── layout.tsx        # Layout base da aplicação
│   ├── page.tsx          # Página principal
├── lib/                  # Funções utilitárias (auth, prisma, etc.)
├── prisma/               # Schema e seed do banco
├── prompts/              # Documentação interna e requisitos
├── public/               # Assets públicos
├── package.json          # Dependências e scripts
├── tsconfig.json         # Configuração TypeScript
```

## Principais Fluxos

- **Agendamento de Serviço**: Usuário seleciona serviço, data e horário, visualiza informações detalhadas e confirma reserva.
- **Autenticação**: Login seguro via BetterAuth, com integração ao backend.
- **Listagem de Barbearias e Serviços**: Exibição dinâmica, com componentes otimizados e responsivos.

## Padrões e Boas Práticas

- Componentização máxima: todo código repetido vira componente ou utilitário.
- UI fiel ao Figma: todos detalhes visuais seguem o design original.
- Cores: apenas variáveis do tema em `globals.css`, nunca hard-coded.
- Scroll horizontal: sempre oculta barra de scroll visual.
- Header/Footer: sempre usando componentes dedicados, nunca criados manualmente.
- Documentação e prompts: requisitos e decisões técnicas registrados em `prompts/`.

## Como Rodar Localmente

1. Instale as dependências:
   ```cmd
   npm install
   ```
2. Configure o banco de dados Postgres e o arquivo `.env` conforme o schema Prisma.
3. Execute as migrações e o seed:
   ```cmd
   npx prisma migrate dev
   npx prisma db seed
   ```
4. Inicie o servidor de desenvolvimento:
   ```cmd
   npm run dev
   ```
5. Acesse `http://localhost:3000` no navegador.

## Contribuição

- Siga os padrões de componentes e estilos definidos.
- Sempre consulte os arquivos em `prompts/` para requisitos e decisões de arquitetura.
- Pull requests devem ser claros, testados e documentados.

## Licença

Este projeto está sob licença MIT.

---

> Para dúvidas, sugestões ou contribuições, abra uma issue ou envie um pull request.
