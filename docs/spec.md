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
        string marca "Ex: Hot Wheels"
        string raridade "Ex: STH, RLC, Mainline"
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
```
## 🏗️ Especificações Técnicas

### Front-end
- **Framework CSS:** Bootstrap v5.3.3 (via CDN).
  - *Motivo:* Uso de variáveis de CSS nativas para o tema "Racing Tech" e Grid System para o Hangar.
- **Ícones:** Google Material Symbols Outlined (v400).
- **Fontes:** Space Grotesk (Headlines) e Rajdhani (Technical Data) via Google Fonts.

### Integrações (APIs)
- **ViaCEP API (v1):** Utilizada no formulário de cadastro de perfil para autocompletar o endereço do colecionador (Setor de Coleção).
  - *Endpoint:* `https://viacep.com.br/ws/{cep}/json/`

