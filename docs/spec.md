### Modelo de Dados (ERD)

```mermaid
erDiagram
    USUARIO ||--o{ MINIATURA : coleciona
    SERIE ||--o{ MINIATURA : contem
    CATEGORIA ||--o{ SERIE : agrupa
    USUARIO ||--o{ LISTA_DESEJOS : planeja

    USUARIO { 
        string id PK
        string nome
        string email
    }

    MINIATURA {
        string id PK
        string nome_modelo
        string numero_serie
        string cor_principal
        int ano_lancamento
        string serie_id FK
    }

    SERIE {
        string id PK
        string nome_serie
        int total_na_colecao
        string categoria_id FK
    }

    CATEGORIA {
        string id PK
        string tipo "Ex: Mainline, STH, Premium"
    }

    LISTA_DESEJOS {
        string id PK
        string usuario_id FK
        string nome_modelo
        string prioridade "Alta/Baixa"
    }
