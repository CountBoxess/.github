<p align="center">
<img src="../public/aaaa.jpeg">
</p>

O CountBoxes tem como função auxiliar na contagem de cargas durante o carregamento ou descarregamento de Mercadorias.

#### Ferramentas

- [Node.js](https://nodejs.org/pt)
- [React](https://react.dev)
- [PostgreSQL](https://www.postgresql.org)
- [PrismaORM](https://www.prisma.io)
- [Yup](https://www.npmjs.com/package/yup)

#### Sobre

O CountBoxes é um aplicativo desenvolvido principalmente com JavaScript, que visa otimizar a contagem de caixas durante o processo de carregamento e descarregamento de cargas em empresas. Ele integra um scanner para registrar e atualizar em tempo real o status dos produtos em ordens de pedidos, proporcionando maior eficiência e precisão na logística.

#### Funcionamento
O gerente cria uma nova ordem de pedidos, onde pode adicionar diversos produtos que serão carregados ou descarregados. Os funcionários responsáveis pelo carregamento ou descarregamento podem visualizar as ordens de pedidos disponiveis para eles. O funcionário pode selecionar uma ordem de pedido específica para visualizar os produtos que precisam ser manipulados. Após abrir a ordem, o funcionário pode começar o processo de escaneamento, utilizando o scanner do aplicativo mobile para registrar os produtos que foram carregados ou descarregados.

#### Funcionalidades:

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

##### Como funciona


#### Padrão de Projeto
##### Singleton

 - O Singleton é um padrão de projeto de software que garante a existência de apenas uma instância de uma classe, mantendo um ponto global de acesso ao seu objeto.

 - Em nosso projeto, utilizamos o Singleton na instanciação do cliente do prisma, assim garantindo que toda a API acesse um unico objeto desse cliente. Caso não fosse utilizado, poderia haver uma grande perda de desempenho, visto que a instanciação é um processo muito custoso para a aplicação.

 - Caso queira ver como está implementado, acesse `countboxes-api/prisma/client`

#### Intruções de uso

- Os comandos para rodar o programa são:
  - `npm install`
  - `npm start`
