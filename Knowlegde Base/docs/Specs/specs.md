# Especificações (Specs) da Plataforma Palmer

## EPIC 1 – Cadastro e Gestão de Faculdades (Backoffice / Catálogo)

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 1.1 | Como **admin**, quero cadastrar faculdades individualmente ou por importação em lote, para manter o catálogo atualizado. | - Formulário de cadastro com todos os campos obrigatórios.<br>- Upload de CSV/Excel para importação em lote.<br>- Validação de dados (CNPJ, e‑mail, etc.). |
| 1.2 | Como **admin**, preciso visualizar a descrição institucional completa, para que os usuários finais vejam detalhes sobre a faculdade. | - Página de detalhes com texto, imagens e biografia.<br>- Renderização responsiva. |
| 1.3 | Como **admin**, quero registrar as notas oficiais do MEC (CI, IGC, Conceito) e exibi‑las publicamente. | - Campos de nota no cadastro.<br>- Exibição em destaque na página da faculdade. |
| 1.4 | Como **admin**, desejo gerenciar a galeria de imagens e vídeos promocionais. | - Upload múltiplo de fotos e vídeos.<br>- Reproductor integrado na página da faculdade. |
| 1.5 | Como **admin**, preciso vincular cursos à faculdade e detalhar grade curricular, horários, duração, mensalidade e bolsas. | - CRUD de cursos dentro da faculdade.<br>- Tabelas de grade curricular, calendário de turnos e tabelas de bolsas. |
| 1.6 | Como **admin**, devo indicar se a faculdade aceita SISU, FIES, ProUni e marcar se o curso é 100 % gratuito. | - Flags (checkbox) para cada programa.<br>- Exibição visual de “gratuito”. |
| 1.7 | Como **admin**, quero publicar o calendário de vestibulares e notas de corte aproximadas. | - Calendário com datas e filtros por curso.<br>- Campo de nota de corte por modalidade. |
| 1.8 | Como **admin**, preciso que faculdades possam ser cadastradas mesmo sem adesão prévia. | - Opção “ativar após cadastro”. |

## EPIC 2 – Cadastro e Perfil do Aluno

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 2.1 | Como **novo aluno**, quero me cadastrar usando e‑mail + senha ou login social (Google, Apple, Facebook). | - Formulário de registro com validação de e‑mail.<br>- Integração OAuth para os provedores. |
| 2.2 | Como **aluno**, desejo editar meu perfil (nome, foto, bio, cidade, curso de interesse). | - Tela de perfil editável.<br>- Upload de avatar. |
| 2.3 | Como **aluno**, preciso recuperar senha caso a esqueça. | - Fluxo “esqueci a senha” via e‑mail com token expiração. |
| 2.4 | Como **aluno**, devo definir meu status acadêmico (Vestibulando, Matriculado, Ex‑aluno). | - Dropdown de status visível no perfil. |
| 2.5 | Como **aluno**, quero vincular meu perfil a uma faculdade após matrícula. | - Busca de faculdade + botão “Vincular”. |

## EPIC 3 – Busca, Filtros e Navegação

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 3.1 | Como **usuário**, quero buscar faculdades, cursos ou cidades a partir de uma barra global. | - Busca “type‑ahead” com sugestões.<br>- Resultado paginado. |
| 3.2 | Como **usuário**, preciso filtrar faculdades por faixa de mensalidade e por programa (SISU, FIES, etc.). | - Slider de preço + checkboxes de programas. |
| 3.3 | Como **usuário**, quero ordenar resultados por preço, nota MEC ou avaliação dos alunos. | - Dropdown de ordenação. |
| 3.4 | Como **aluno**, desejo deixar comentários e avaliações nas páginas das faculdades. | - Sistema de avaliação 1‑5 estrelas + campo de comentário.<br>- Média calculada e exibida. |
| 3.5 | Como **aluno**, preciso salvar faculdades como “Objetivos” e ver quantos outros usuários também salvaram. | - Botão “Favoritar”.<br>- Contador de usuários. |
| 3.6 | Como **usuário**, quero ver na Home os cursos em destaque, descontos e depoimentos. | - Carrossel responsivo com cards de cursos/descontos.<br>- Seção de depoimentos. |
| 3.7 | Como **usuário**, preciso de atalho rápido para busca por estado e cidade. | - Links de filtro rápido na Home. |

## EPIC 4 – Processo de Matrícula Integrada

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 4.1 | Como **aluno**, devo iniciar a matrícula diretamente da página da faculdade. | - Botão “Iniciar Matrícula”. |
| 4.2 | Como **aluno**, preciso preencher formulário com dados pessoais e fazer upload de documentos (RG, CPF, Histórico, Comprovante). | - Formulário multi‑step com validações de arquivo (tipo, tamanho). |
| 4.3 | Como **aluno**, quero pagar a taxa de matrícula ou 1ª mensalidade via gateway integrado. | - Integração com Stripe/PayPal (exemplo). |
| 4.4 | Como **aluno**, devo receber comprovante PDF da pré‑matrícula. | - Geração automática de PDF e e‑mail de entrega. |
| 4.5 | Como **admin**, preciso de um painel para acompanhar todas as matrículas recebidas. | - Dashboard com lista, status e filtros. |

## EPIC 5 – Portfólio de Projetos do Aluno

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 5.1 | Como **aluno**, quero cadastrar projetos com título, descrição, imagens, arquivos e links externos. | - Formulário de projeto com upload de mídia e campos de URLs. |
| 5.2 | Como **aluno**, preciso marcar a faculdade/curso associado ao projeto e adicionar tags de competências. | - Campos de seleção de faculdade/curso + tag input. |
| 5.3 | Como **aluno**, desejo que meu portfólio seja público e compartilhável. | - URL pública read‑only e botão “Compartilhar”. |
| 5.4 | Como **recrutador**, quero visualizar portfólios de alunos. | - Busca de usuários → visualização de portfólio público. |

## EPIC 6 – Repositório de Materiais de Aula

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 6.1 | Como **aluno**, posso fazer upload de materiais (PDF, imagens, etc.) e categorizá‑los por disciplina, período e faculdade. | - Upload com metadados (disciplina, semestre, faculdade). |
| 6.2 | Como **aluno**, desejo pré‑visualizar o conteúdo antes de baixar. | - Viewer embutido para PDF/imagens. |
| 6.3 | Como **aluno**, posso buscar materiais por disciplina ou palavra‑chave. | - Busca textual usando Elasticsearch. |

## EPIC 7 – Rede Social e Networking

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 7.1 | Como **aluno**, quero um feed de notícias com projetos e materiais recentes. | - Feed escrolável, ordenado por data. |
| 7.2 | Como **aluno**, posso seguir outros usuários e curtir/reagir a publicações. | - Botões “Seguir”, “Curtir”, “Reagir”. |
| 7.3 | Como **aluno**, devo comentar e compartilhar projetos em redes externas (LinkedIn, WhatsApp). | - Botões de compartilhamento com links de OG. |
| 7.4 | Como **empresa**, posso consultar portfólios de alunos. | - Área B2B com busca por competências. |
| 7.5 | Como **aluno**, preciso de chat privado para trocar mensagens com outros usuários. | - Sistema de mensagens em tempo‑real (WebSocket). |

## EPIC 8 – Notificações e Comunicação

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 8.1 | Como **sistema**, envio e‑mail de confirmação de cadastro e recuperação de senha. | - E‑mail com link de confirmação / reset (expira 24h). |
| 8.2 | Como **sistema**, notifico sobre prazos de vestibular, bolsas e status de matrícula. | - Notificações push + e‑mail. |
| 8.3 | Como **aluno**, recebo alerta quando meu projeto recebe curtidas/comentários. | - Notificação in‑app e opcional por e‑mail. |

## EPIC 9 – Painel Administrativo e Métricas

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 9.1 | Como **admin**, visualizo total de visualizações por faculdade/curso. | - Gráficos de tráfego (daily/weekly). |
| 9.2 | Como **admin**, gero relatório de conversão de cliques → intenção de matrícula. | - Exportação CSV. |
| 9.3 | Como **admin**, aprovo/reprovo projetos e materiais denunciados. | - Workflow de moderação com status (Aprovado, Rejeitado, Em revisão). |
| 9.4 | Como **admin**, listam‑se termos de busca sem resultados para identificar oportunidades de conteúdo. | - Lista de “search gaps”. |

## EPIC 10 – Vitrine Pública das Faculdades

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 10.1 | Como **visitante**, acesso a página de cada faculdade sem necessidade de login. | - Page pública, SEO‑friendly. |
| 10.2 | Como **visitante**, vejo imagens de eventos e galeria institucional. | - Galeria responsiva. |

## EPIC 11 – Vitrine de Moradias Estudantis

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 11.1 | Como **aluno**, visualizo imóveis próximos ao campus em mapa interativo. | - Integração com Google Maps / Leaflet.<br>- Filtro por raio (1 km, 5 km…). |
| 11.2 | Como **aluno**, filtro por preço, modalidade, pet‑friendly e calculo tempo de deslocamento. | - Slider de preço + checkboxes.<br>- API de rotas (Google Directions). |
| 11.3 | Como **plataforma**, exibo aviso de isenção de responsabilidade sobre anúncios. | - Banner fixo nas páginas de moradia. |

## EPIC 12 – Mercado de Trabalho Inteligente

| # | User Story | Critérios de Aceitação |
|---|------------|------------------------|
| 12.1 | Como **sistema**, mapeio curso do aluno → tags de mercado (ex.: Medicina → “Veterinário”). | - Algoritmo de mapeamento configurável. |
| 12.2 | Como **aluno**, vejo vagas filtradas por curso e sub‑área de interesse. | - Filtro avançado no painel de vagas. |
| 12.3 | Como **aluno**, posso candidatar‑me usando meu portfólio Palmer. | - Botão “Candidatar‑se com perfil Palmer”. |
| 12.4 | Como **empresa**, publico vagas via painel B2B e integro com APIs externas. | - CRUD de vagas + webhook para agregadores. |
| 12.5 | Como **sistema**, calculo % de compatibilidade entre vaga e perfil do aluno. | - Scoring baseado em tags/competências. |
| 12.6 | Como **aluno**, recebo alerta quando novas vagas compatíveis são publicadas. | - Notificação push + e‑mail. |
| 12.7 | Como **aluno**, acompanho status da candidatura (Enviado, Em Análise, Entrevista, Finalizado). | - Timeline de status na página da vaga. |

---

### Próximos passos
1. **Priorizar épicos** (ex.: começar pelos módulos de cadastro e busca).  
2. **Criar histórias de usuário detalhadas** a partir das specs acima, atribuindo *story points* e *sprints*.  
3. **Alinhar com a equipe de desenvolvimento** para definir arquitetura de dados e APIs necessárias.  

Caso queira incluir mais detalhes (ex.: diagramas de fluxo, modelos de dados, ou um backlog de *stories* pronto), só avisar que eu gero o artefato! 🚀