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

10. Clique em **Create connection** (Criar conexão) e/ou **Connect**.

> **Nota:** Anote o nome da conexão, pois ele será usado na configuração do pipeline.

---

### 2. Criar um Pipeline e Configurar a Fonte do Repositório

1. No console do **AWS CodePipeline**, clique em **Create pipeline** (Criar pipeline).
2. Dê um nome ao pipeline e clique em **Next** (Próximo).
3. Em **Source provider** (Provedor de origem), selecione **CodeStar Connections**.
4. Escolha a conexão criada anteriormente.
5. Selecione o repositório e o branch que deseja usar como origem.
6. Clique em **Next** (Próximo) para continuar a configurar as etapas do pipeline (build, deploy, etc.).

---

## Dicas e Boas Práticas

- Certifique-se de que as permissões do repositório permitem acesso ao aplicativo AWS CodePipeline.
- Para repositórios privados, configure as credenciais de acesso (tokens ou chaves SSH) corretamente.
- Use **IAM roles** para restringir permissões e melhorar a segurança.
- Teste a conexão antes de implementar o pipeline completo.

---

## Resolução de Problemas

### Erro: "Permission Denied"
- Verifique se o token ou a autorização para o repositório está configurado corretamente.

### Erro: "Connection Not Found"
- Certifique-se de que a conexão foi criada no mesmo região em que o pipeline está sendo configurado.

---

## Referências

- [Documentação Oficial do AWS CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html)
- [Conexão com Repositórios Git](https://docs.aws.amazon.com/codepipeline/latest/userguide/connections-github.html)
- [Boas Práticas de Segurança na AWS](https://aws.amazon.com/pt/architecture/security-identity/)

---

Seguindo este guia, você será capaz de configurar uma conexão entre o AWS CodePipeline e seu repositório Git de forma rápida e segura.
