<p align="center">
<img src="../public/aaaa.jpeg">
</p>

#### Visão geral

O countBoxes é um aplicativo desenvolvido principalmente com JavaScript, que visa para otimizar a contagem de caixas durante o processo de carregamento e descarregamento de cargas em empresas. Ele integra um scanner para registrar e atualizar em tempo real o status dos produtos em ordens de pedidos, proporcionando maior eficiência e precisão na logística.

#### Ferramentas

- [Node.js](https://nodejs.org/pt)
- [React](https://react.dev)
- [PostgreSQL](https://www.postgresql.org)
- [PrismaORM](https://www.prisma.io)
- [Yup](https://www.npmjs.com/package/yup)

### Funcionalidades

1. **Escaneamento de produtos**
   - O aplicativo permite o escaneamento de códigos de barra para registrar o produto correspondente e atualizar automaticamente a contagem de itens em uma ordem de pedido.
2. **Atualização em tempo real**

   - Cada vez que um produto é escaneado, a contagem é atualizada em tempo real.

3. **Divisão de contas**

   - O aplicativo divide as contas entre funcionário e gerente. Isso permite que somente a conta do gerente tenha acesso a funcionalidades específicas.

4. **Operações de CRUD**
   O aplicativo oferece a capacidade de **criar**, **buscar**, **atualizar** e **deletar** os seguintes componentes:

   - Veículo
   - Cliente
   - Ordem
   - Produto
   - Usuário
   - Carga

5. **Validações**
   - Se necessário, determinados campos são validados utilizando o **Yup**, garantindo que os dados inseridos atendam aos critérios exigidos antes de serem processados.

### Padrão de Projeto
#### Singleton

 - O Singleton é um padrão de projeto de software que garante a existência de apenas uma instância de uma classe, mantendo um ponto global de acesso ao seu objeto.

 - Em nosso projeto, utilizamos o Singleton na instanciação do cliente do prisma, assim garantindo que toda a API acesse um unico objeto desse cliente. Caso não fosse utilizado, poderia haver uma grande perda de desempenho, visto que a instanciação é um processo muito custoso para a aplicação.

 - Caso queira ver como está implementado, acesse `countboxes-api/prisma/client`

### Intruções de uso

- Padrão de projeto: **Singleton** no Prisma.
- Os comandos para rodar o programa são:
  - `npm install`
  - `npm start`
