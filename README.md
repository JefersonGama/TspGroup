# Sistema de Gerenciamento TSP

Este é um sistema web desenvolvido em HTML, CSS e JavaScript, integrado ao Supabase para persistência de dados e autenticação. Ele permite a gestão de avisos, técnicos e produção em uma fábrica, com áreas distintas para administradores e técnicos.

## 📁 Estrutura de Pastas

Sistema-Gerencia-TSP/
│
├── index.html (Página de Login)
├── README.md
│
├── admin/
│ ├── dashboard.html
│ ├── relatorios.html
│ ├── avisos.html
│ ├── producao-tecnico.html
│ ├── tecnicos.html
│ └── components/
│ ├── modal-novo-aviso.html
│ ├── modal-editar-aviso.html
│ ├── modal-adicionar-tecnico.html
│ └── modal-producao-diaria.html
│
├── tecnico/
│ ├── dashboard.html
│ ├── avisos.html
│ ├── perfil.html
│ └── components/
│ └── card-aviso.html
│
├── assets/
│ ├── css/
│ │ ├── styles.css
│ │ ├── admin.css
│ │ ├── tecnico.css
│ │ ├── login.css
│ │ └── responsive.css
│ ├── js/
│ │ ├── supabase-config.js
│ │ ├── auth.js
│ │ ├── admin-dashboard.js
│ │ ├── admin-relatorios.js
│ │ ├── admin-avisos.js
│ │ ├── admin-tecnicos.js
│ │ ├── admin-producao.js
│ │ ├── tecnico-dashboard.js
│ │ ├── tecnico-avisos.js
│ │ ├── tecnico-perfil.js
│ │ └── notifications.js
│ ├── images/
│ └── data/
│ └── mock-data.js
│
├── supabase/
│ ├── database/
│ │ ├── schema.sql
│ │ ├── policies.sql
│ │ ├── functions.sql
│ │ ├── triggers.sql
│ │ └── seed-data.sql
│ ├── storage/
│ └── supabase-config.js
│
└── utils/
├── date-helpers.js
├── form-validators.js
├── export-pdf.js
└── charts-config.js


## ⚙️ Configuração do Supabase

1.  Crie um projeto no [Supabase](https://supabase.com/).
2.  Anote a **Project URL** e a **Anonymous Key** (Anon Key).
3.  Atualize os valores no arquivo `supabase/supabase-config.js`:

    ```javascript
    const SUPABASE_URL = 'SUA_URL_AQUI';
    const SUPABASE_ANON_KEY = 'SUA_ANON_KEY_AQUI';
    ```

4.  Execute os scripts SQL contidos na pasta `supabase/database/` no editor SQL do painel do Supabase:
    -   `schema.sql`: Cria as tabelas.
    -   `policies.sql`: Habilita e define as políticas de segurança (RLS).

## 🎨 Cores Padrão

-   **Verde Principal:** `#BADA52` (RGB: 186, 218, 82)
-   **Azul Secundário:** `#64C4DF` (RGB: 100, 196, 223)

## 🚀 Funcionalidades

### Área do Administrador

-   **Dashboard:** Visão geral com métricas.
-   **Relatórios:** Geração de relatórios com gráficos e filtros de data.
-   **Avisos:** Listagem, cadastro, edição e exclusão de avisos. Atribuição a técnicos.
-   **Técnicos:** Cadastro, listagem, edição e exclusão de técnicos. Criação automática de conta de usuário.
-   **Produção:** Gerenciamento de registros diários de produção por técnico.

### Área do Técnico

-   **Dashboard:** Métricas e avisos atribuídos.
-   **Meus Avisos:** Lista apenas os avisos atribuídos ao técnico logado.
-   **Perfil:** Visualização e edição de dados pessoais e senha.

## 🛠️ Tecnologias Utilizadas

-   **Frontend:** HTML5, CSS3, JavaScript (ES6+)
-   **Bibliotecas:** Chart.js (gráficos), jsPDF (exportação de PDF)
-   **Backend/DBaaS:** [Supabase](https://supabase.com/) (PostgreSQL, Auth, RLS)

## 📝 Licença

[Escolha uma licença, por exemplo, MIT]