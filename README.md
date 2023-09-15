<h1 align="center" id="title">Labeddit Backend</h1>


DOCUMENTAÇÃO: https://documenter.getpostman.com/view/24823235/2s9XxyRtDt

LINK REPOSITORIO BACKEND: https://github.com/ricardodaantas/labeddit-back

LINK REPOSITORIO FRONTEND: https://github.com/ricardodaantas/labeddit-front

LINK DO SITE SURGE: https://ricardo-dantas-labeddit.surge.sh/

LINK API NO RENDER: https://ricardo-dantas-labeddit.onrender.com

  
<h2>🧐 Funcionalidades</h2>

O backend do Labeddit possui as seguintes funcionalidades:

*   Cadastro/Login de Usuáriosg
*   Criação Edição e Exclusão de Posts e Comentários
*   Interagir com os Posts e seus respectivos Comentários (Likes e Dislikes)

<h2>🛠️ Passos para Instação:</h2>

Para configurar o projeto em sua máquina local, siga os passos abaixo:

<p>1. Clonar o repositório:</p>

```
git clone https://github.com/rafaelmelodruzian/labeddit-back-end.git
```

<p>2. Acessar a pasta do projeto:</p>

```
cd labeddit-back-end
```

<p>3. Instalar as dependências:</p>

```
npm install
```

<p>4. Configurar variáveis de ambiente:</p>

```
PORT=3003 DB_FILE_PATH=./src/database/labeddit.db JWT_KEY=sua-senha JWT_EXPIRES_IN=7d BCRYPT_COST=12
```

<p>5. Crie as tabelas do banco usando o arquivo labeddit.sql</p>

<p>6. Inicie o servidor:</p>

```
npm run dev
```

  
<h2>🔚 Endpoints</h2>

### Usuários

1. **Cadastro de Usuários (POST)**
   - URL: `http://localhost:3003/users/signup`
   - Descrição: Permite que os usuários se cadastrem na plataforma Labeddit.

2. **Login de Usuários (POST)**
   - URL: `http://localhost:3003/users/login`
   - Descrição: Permite que os usuários façam login na plataforma Labeddit.

3. **Obter o ID do Usuário (GET)**
   - URL: `http://localhost:3003/users/`
   - Descrição: Permite que os usuários obtenham o ID do usuário autenticado com base no Token JWT.

### Publicações

4. **Obter Todos os Posts (GET)**
   - URL: `http://localhost:3003/posts/`
   - Descrição: Permite que os usuários obtenham todos os posts existentes na plataforma Labeddit.

5. **Obter Post por ID (GET)**
   - URL: `http://localhost:3003/posts/:id`
   - Descrição: Permite que os usuários obtenham informações detalhadas sobre um post específico com base no ID fornecido.

6. **Criar um Novo Post (POST)**
   - URL: `http://localhost:3003/posts/`
   - Descrição: Permite que os usuários criem um novo post na plataforma Labeddit.

7. **Editar um Post Existente (PUT)**
   - URL: `http://localhost:3003/posts/:id`
   - Descrição: Permite que os usuários editem o conteúdo de um post existente com base no ID fornecido.

8. **Excluir um Post (DELETE)**
   - URL: `http://localhost:3003/posts/:id`
   - Descrição: Permite que os usuários excluam um post específico na plataforma Labeddit.

9. **Interagir com um Post (Like/Dislike) (PUT)**
   - URL: `http://localhost:3003/posts/:id/like`
   - Descrição: Permite que os usuários interajam com os posts através das ações de "like" e "dislike".

10. **Verificar Reação do Usuário em um Post (GET)**
    - URL: `http://localhost:3003/posts/:id/checklike`
    - Descrição: Permite que os usuários obtenham a reação registrada para um post específico com base no ID fornecido.

### Comentários

11. **Obter Todos os Comentários de um Post (GET)**
    - URL: `http://localhost:3003/comments/:id`
    - Descrição: Permite que os usuários obtenham todos os comentários existentes para um post específico.

12. **Criar um Novo Comentário em um Post (POST)**
    - URL: `http://localhost:3003/comments/:id`
    - Descrição: Permite que os usuários criem um novo comentário em um post específico.

13. **Editar um Comentário Existente (PUT)**
    - URL: `http://localhost:3003/comments/:id`
    - Descrição: Permite que os usuários editem o conteúdo de um comentário existente com base no ID fornecido.

14. **Excluir um Comentário (DELETE)**
    - URL: `http://localhost:3003/comments/:id`
    - Descrição: Permite que os usuários excluam um comentário específico na plataforma Labeddit.

15. **Interagir com um Comentário (Like/Dislike) (PUT)**
    - URL: `http://localhost:3003/comments/:id/like`
    - Descrição: Permite que os usuários interajam com os comentários através das ações de "like" e "dislike".

16. **Verificar Reação do Usuário em um Comentário (GET)**
    - URL: `http://localhost:3003/comments/:id/checklike`
    - Descrição: Permite que os usuários obtenham a reação registrada para um comentário específico com base no ID fornecido.
