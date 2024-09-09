<p align="center">
<img src="../public/aaaa.jpeg">
</p>

O CountBoxes tem como função auxiliar na contagem de cargas durante o carregamento ou descarregamento de mercadorias.

#### Ferramentas

- [Node.js](https://nodejs.org/pt)
- [React](https://react.dev)
- [PostgreSQL](https://www.postgresql.org)
- [PrismaORM](https://www.prisma.io)
- [Yup](https://www.npmjs.com/package/yup)

#### Sobre

O CountBoxes é um aplicativo desenvolvido principalmente com JavaScript, que visa otimizar a contagem de caixas durante o processo de carregamento e descarregamento de cargas em empresas. Ele integra um scanner para registrar e atualizar em tempo real o status dos produtos em ordens de pedidos, proporcionando maior eficiência e precisão na logística. Com o CountBoxes, o processo de contagem de caixas se torna auditável e totalmente digitalizado, facilitando o controle de inventário.

#### Funcionamento
Funcionamento
1. O gerente cria uma nova ordem de pedidos, onde pode adicionar diversos produtos que serão carregados ou descarregados.
   
2. Os funcionários responsáveis pelo carregamento ou descarregamento podem visualizar as ordens de pedidos disponíveis para eles.
   
3. Ao selecionar uma ordem de pedido específica, o funcionário pode visualizar os produtos que precisam ser manipulados.
   
4. O funcionário inicia o processo de escaneamento, utilizando o scanner do aplicativo para registrar os produtos que foram carregados ou descarregados. Cada escaneamento atualiza automaticamente a contagem em tempo real.

#### Funcionalidades:

1. **Escaneamento de produtos**
   - O aplicativo permite o escaneamento de códigos de barra para registrar o produto correspondente e atualizar automaticamente a contagem de itens em uma ordem de pedido.
     
2. **Atualização em tempo real**
   - Cada vez que um produto é escaneado, a contagem é atualizada em tempo real, facilitando o acompanhamento do processo.

3. **Divisão de contas**
   - O aplicativo divide as contas entre funcionários e gerentes. Isso permite que apenas o gerente tenha acesso a funcionalidades específicas, como a criação de ordens de pedido ou a remoção de produtos.

4. **Operações de CRUD**
    O aplicativo oferece a capacidade de Criar, Ler, Atualizar e Deletar os seguintes componentes:
   - Veículo
   - Cliente
   - Ordem
   - Produto
   - Usuário
   - Carga

5. **Validações**
   - Determinados campos são validados utilizando o Yup, garantindo que os dados inseridos atendam aos critérios exigidos antes de serem processados. Isso inclui, por exemplo, a validação do CNPJ na criação de clientes.

#### Padrão de Projeto
##### Singleton

 - O Singleton é um padrão de projeto de software que garante a existência de apenas uma instância de uma classe, mantendo um ponto global de acesso ao seu objeto.

 - Em nosso projeto, utilizamos o Singleton na instanciação do cliente do prisma, assim garantindo que toda a API acesse um unico objeto desse cliente. Sem a implementação do padrão Singleton, várias instâncias do cliente Prisma poderiam ser criadas, o que aumentaria o consumo de memória e a complexidade do gerenciamento de conexões, gerando perda de desempenho.

 - Caso queira ver como está implementado, acesse `countboxes-api/prisma/client`

#### Intruções de uso

- Os comandos para rodar o programa são:
  - `npm install`
  - `npm start`
