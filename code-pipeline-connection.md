# Documentação: Criar uma Conexão no AWS CodePipeline com um Repositório no Git

Configuração de uma conexão entre o AWS CodePipeline e um repositório no Git.

---

## Pré-requisitos

Antes de começar, certifique-se de ter:

1. Um repositório Git configurado no GitHub, GitLab ou outro provedor.
2. Permissões apropriadas para criar pipelines no AWS CodePipeline e no repositorio Git (precisa instalar o app de conexao no repo).
3. Acesso ao console de gerenciamento da AWS.

---

## Etapas para Configurar a Conexão

### 1. Criar uma Conexão no AWS CodePipeline

1. Acesse o console do **AWS CodePipeline**.
   
   ![image](https://github.com/user-attachments/assets/77a49347-dfb2-454a-bc30-efb69dc4b191)

2. Clique em **Connections** (Conexões) no menu lateral.

  ![image](https://github.com/user-attachments/assets/86025ae7-8ad3-48de-922a-35a2afb7228e)

3. Clique no botão **Create connection** (Criar conexão).

  ![image](https://github.com/user-attachments/assets/fc5516a1-6520-4ebc-9369-09ebf6280b23)

4. Escolha o provedor Git adequado (ex.: **GitHub** ou **GitHub Enterprise Server**).

  ![image](https://github.com/user-attachments/assets/14ea223a-266c-4dae-afea-26436fe39ea6)

5. De um nome a sua conexao.

   ![image](https://github.com/user-attachments/assets/97c944d6-51a0-4f62-bc5a-f5aae7c0ab15)

6. Clique em "Connect to GitHub".

   ![image](https://github.com/user-attachments/assets/9c079cca-ddff-499a-865e-c4c494f17bdb)

7. Clique em **Install a new app** (Instalar um novo aplicativo) para autorizar a conexão entre a AWS e o repositório Git.

  ![image](https://github.com/user-attachments/assets/65f097f9-d5cb-462a-840e-1e1eb2f40725)

  - **GitHub**: Você será redirecionado para a página do GitHub para autorizar o aplicativo AWS CodePipeline.

    ![image](https://github.com/user-attachments/assets/083398d4-ef11-42cd-b6b3-d7ce7aa9c00c)

8. Clique em **Create connection** (Criar conexão) e/ou **Connect**.


---

## Referências

- [Documentação Oficial do AWS CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html)
- [Conexão com Repositórios Git](https://docs.aws.amazon.com/codepipeline/latest/userguide/connections-github.html)
- [Boas Práticas de Segurança na AWS](https://aws.amazon.com/pt/architecture/security-identity/)

