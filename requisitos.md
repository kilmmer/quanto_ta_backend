<h1>Premissa</h1>
O app vai receber os preços de combustíveis a partir dos usuários, eles irão selecionar o posto no mapa e informar o preço do litro do combustível que foi abastecido.
Com base nos preços informados, terão um indicativo de confiabilidade, quanto mais pessoas informarem aquele mesmo valor, mais confiável será aquela informação.
O usuário poderá consultar o menor preço mais próximo dele a partir da informação do gps.
O usuário precisará fazer um login para utilizar o app.
Outros usuários poderão reconfirmar que o último preço informado é válido ainda.

**<h1>Tecnologias</h1>**
1. **Node.js com TypeScript:**
   - Use o Node.js para a execução do servidor e adicione o TypeScript para trazer benefícios de tipagem estática.

2. **Express.js:**
   - Framework web para criar APIs RESTful de forma rápida e eficiente.

3. **Sequelize:**
   - Como ORM para interagir com o PostgreSQL. Facilitará a manipulação de dados no banco de dados.

4. **PostgreSQL:**
   - Banco de dados relacional para armazenar informações sobre preços de combustíveis e usuários.

5. **JWT (JSON Web Tokens):**
   - Para autenticação segura dos usuários.

6. **bcrypt:**
   - Para garantir o armazenamento seguro das senhas dos usuários.

7. **Axios:**
   - Se necessário, para fazer requisições HTTP para serviços externos, como consultas de geolocalização.

8. **Jest ou Mocha/Chai:**
   - Para testes unitários e de integração.

9. **Swagger ou OpenAPI:**
   - Ferramentas para documentar automaticamente a API.

10. **Helmet:**
    - Para melhorar a segurança da sua aplicação Express.js.


**<h1>Requisitos</h1>**


### 1. Cadastro e Login de Usuários:
   - **Cadastro de Usuário:**
     - Endpoint para criar uma nova conta de usuário.
     - Campos necessários: nome, e-mail e senha.
     - Senhas devem ser armazenadas de forma segura usando bcrypt.

   - **Login de Usuário:**
     - Endpoint para autenticar usuários e gerar tokens JWT.
     - Requer verificação de e-mail/senha.

### 2. Input de Preços de Combustíveis:
   - **Endpoint para Inserir Preço:**
     - Permitir que os usuários enviem dados de preço de combustível.
     - Campos necessários: preço, tipo de combustível, localização (latitude e longitude) e identificação do usuário.
     - Validar os dados recebidos.

### 3. Indicativo de Confiabilidade:
   - **Sistema de Confirmação:**
     - Implementar um contador de confirmações por preço registrado.
     - Atualizar a confiabilidade com base nas confirmações recebidas.

### 4. Consulta de Menor Preço Próximo:
   - **Endpoint para Consulta de Preço:**
     - Permitir que os usuários consultem o menor preço de combustível próximo a eles.
     - Utilizar a localização do usuário para encontrar postos próximos.

### 5. Reconfirmação de Preços:
   - **Endpoint para Reconfirmar Preço:**
     - Usuários podem reconfirmar a validade do último preço informado.
     - Atualizar o contador de confirmações correspondente.

### 6. Integração com Mapa:
   - **Integração de Mapa:**
     - Utilizar uma biblioteca ou serviço de mapas (por exemplo, Google Maps API) para facilitar a seleção de postos no mapa.

### 7. Segurança:
   - **Validação de Dados:**
     - Implementar validação de dados para prevenir injeções de SQL e outros tipos de ataques.
     - Garantir que a comunicação entre o cliente e o servidor seja segura (usando HTTPS).

### 8. API RESTful:
   - **Endpoints RESTful:**
     - Projete endpoints seguindo os princípios RESTful para CRUD (Create, Read, Update, Delete) de usuários, preços de combustíveis, etc.

### 9. Documentação Simples:
   - **Documentação da API:**
     - Criar documentação simples explicando cada endpoint, métodos permitidos, parâmetros e formatos de dados esperados.
     - Facilitar o entendimento para desenvolvedores que possam interagir com a API.
