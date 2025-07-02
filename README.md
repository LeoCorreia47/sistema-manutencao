# sistema-manutencao
Sistema de manutenção de equipamentos
## Requisitos

1. **Banco de Dados**: PostgreSQL 16 ou 17.  
2. **Java**: JDK 17.  
3. **Node.js e npm**: Versão compatível com o Angular 17 (verifique a documentação oficial).  
4. **Maven**: Para gerenciamento e execução do backend.  
5. **Angular CLI**: Versão compatível com o Angular 17.  

---

## Configuração

### Banco de Dados
1. Certifique-se de que o PostgreSQL está instalado e em execução.  
2. Configure um banco de dados com o nome `crud`. Caso deseje usar outro nome, será necessário alterar a propriedade `spring.datasource.url` no arquivo `application.properties`.  

### Configuração do Backend
O arquivo `application.properties`, localizado em `backend\sistema-manutencao\src\main\resources\`, contém as configurações do projeto para o banco de dados e envio de e-mails.  

#### Configurações de conexão com o banco:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/crud?useUnicode=true&characterEncoding=UTF-8
spring.datasource.username=postgres
spring.datasource.password=postgres
```

- **Ajuste os parâmetros**: Caso já possua outro usuário ou senha configurados no PostgreSQL, altere as propriedades acima para refletir as suas configurações.  

#### Configurações de e-mail:
```properties
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=w966409@gmail.com
spring.mail.password=pcsz evzq jekf lhxy
```
- Substitua o e-mail e senha acima pelos seus dados reais. O e-mail configurado será utilizado para o envio de senhas criptografadas para novos usuários.  
- **Atenção**: Para usar o Gmail, ative a autenticação de dois fatores na conta e gere uma senha específica para aplicativos.  

### Geração e População do Banco
1. Após configurar o banco de dados, inicie o backend. Na primeira execução, o esquema do banco será gerado automaticamente.  
2. Para popular o banco com dados de teste, execute os scripts contidos no arquivo `data.sql`, localizado em `.\backend\sistema-manutencao\src\main\resources\`.  

---

## Executando o Projeto

### Backend
1. Navegue até a pasta `./backend/sistema-manutencao`.  
2. Execute o seguinte comando:  
   ```bash
   mvn spring-boot:run
   ```  
   - **Dica**: Você também pode utilizar a extensão **Spring Boot Dashboard** no VS Code ou outra IDE compatível para gerenciar o backend de forma gráfica.  

### Frontend
1. Navegue até a pasta `./frontend`.  
2. Instale as dependências com o comando:  
   ```bash
   npm install
   ```  
3. Inicie o servidor do Angular 17 com o comando:  
   ```bash
   ng serve
   ```  
4. Clique no link gerado (geralmente `http://localhost:4200/`) para acessar a interface web.  

---

**Pronto!** Agora você pode acessar a aplicação no navegador e utilizar as funcionalidades disponíveis.

## Documentação
[Manutenção de Equipamentos - 2024-2] https://docs.google.com/document/d/1nBBBqBJEexLQy3j4Em9vQJJ_PS-NXiElNrbWo_Fd7pw/edit?usp=sharing

Exemplo - Diagrama de classes - Backend - CRUD Funcionário
![dc_back_exemplo](https://github.com/user-attachments/assets/5333ceb3-3fb8-4a65-afbb-81b9befb207f)

Exemplo - Diagrama de classes - Frontend - CRUD Funcionário
![dc_front_exemplo](https://github.com/user-attachments/assets/519be627-0704-437d-af35-423310fd9537)
