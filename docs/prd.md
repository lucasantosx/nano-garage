# **📄 Product Requirements Document (PRD) - NanoGarage - Catálogo Web de Gerenciamento de Miniaturas 1/64**

**Autor: Lucas Santos de Lima**

Com o crescimento do mercado de colecionáveis, especialmente miniaturas 1:64 como Hot Wheels, muitos usuários possuem centenas de itens, dificultando o controle de quais
modelos já possuem, quais são as raridades (STH, RLC, Chase) e quais lotes estão completos. A falta de uma ferramenta centralizada que una a consulta de lançamentos de 
2026 e anos anteriores com uma gestão de uma coleção física pessoal gera desorganização.
Dessa forma, o Nano Garage surge como uma plataforma web de alta fidelidade visual (Estilo Apple) que permita ao colecionador catalogar sua 'Garagem Virtual', separar
itens por raridade e consultar dados técnicos de miniaturas.

# **2. Atores do Sistema**
**Visitante:**  Usuário acessa a aplicação para explorar o catálogo público de lançamentos, visualizar detalhes técnicos e buscar miniaturas específicas via API.

**Colecionador (Usuário):** Usuário autenticado que pode gerenciar sua própria garagem, adicionar miniaturas à sua coleção física virtual, filtrar por raridade e 
alternar preferências de interface (Modo Noturno).

# **3. Histórias de Usuários e Escopo**

# **🏎️Épico 1: Exploração de Raridades**
- **US01 - Listar Lançamentos:** Como um Visitante, quero visualizar os modelos dos lotes de 2026 com badges de raridade, para identificar quais carros quero caçar.
  - **Critérios de Aceitação:** Os dados devem vir de uma API; layout em Grid responsivo (ID 02/03); badges coloridos por categoria (ID 06).
- **US02 - Buscar Miniaturas:** Como um Visitante, quero pesquisar carrinhos pelo nome ou lote, para encontrar modelos específicos rapidamente.
  - **Critérios de Aceitação:** Filtro dinâmico via JavaScript/jQuery (ID 20); funcionamento com nomes parciais.
- **US03 - Detalhes Premium:** Como um Visitante, quero ver as especificações de um carro (tipo de pneu, pintura Spectraflame), para entender por que ele é uma raridade.
  - **Critérios de Aceitação:** Exibição em Modal minimalista (ID 04); uso de imagens WebP otimizadas (ID 10).
 
# **🏠Épico 2: Minha Garagem (Biblioteca)**
- **US04 - Adicionar à Coleção:** Como um Colecionador, quero salvar uma miniatura no meu perfil, para registrar que ela faz parte da minha coleção física.
  - **Critérios de Aceitação:** Persistência no JSON Server (ID 22); impedir duplicatas no perfil do usuário.
- **US05 - Visualizar Garagem Pessoal:** Como um Colecionador, quero ver apenas os carros que eu possuo, para exibir meu acervo para outros.
  - **Critérios de Aceitação:** Carregamento assíncrono do JSON Server filtrado por usuário (ID 23); layout fluido com unidades relativas (ID 05).
- **US06 - Gerenciar Acervo:** Como um Colecionador, quero remover ou editar o estado de um item (ex: de 'Loose' para 'MOC'), para manter meu inventário preciso.
  - **Critérios de Aceitação:** Atualização imediata na interface e no servidor via DELETE/PUT.

# **🔐Épico 3: Experiência do Usuário e Cadastro**
- **US07 - Cadastro com Localização:** Como um Visitante, quero me cadastrar informando meu CEP, para que meu endereço seja preenchido automaticamente.
  - **Critérios de Aceitação:** Integração real com API ViaCEP (ID 24); validação de campos obrigatórios e máscaras jQuery (ID 11, 21).
- **US08 - Validação de Segurança:**  Como um Colecionador, quero que minha senha siga padrões de segurança, para proteger os dados da minha coleção valiosa.
  - **Critérios de Aceitação:** Validação customizada via REGEX (ID 12); feedback de erro visual no formulário.
- **US09 - Modo Noturno (Apple Style):** Como um Colecionador, quero alternar para o tema escuro, para navegar na minha garagem à noite com elegância.
  - **Critérios de Aceitação:** Troca de classes via jQuery (ID 20); preferência salva no LocalStorage (ID 14).
  

