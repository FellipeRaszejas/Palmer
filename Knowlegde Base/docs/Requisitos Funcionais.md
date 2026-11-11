# Requisitos Funcionais da Plataforma Palmer

## Módulo 1 – Cadastro e Gestão de Faculdades (Backoffice / Catálogo)
1. Cadastro de faculdades via painel de administração ou importação em lote.
2. Exibição da descrição institucional detalhada.
3. Exibição da biografia (história, missão e diferenciais).
4. Cadastro e exibição das notas oficiais do MEC (CI, IGC e Conceito Curso).
5. Galeria de imagens para divulgação do campus e infraestrutura.
6. Integração de reprodutor de vídeos promocionais e institucionais.
7. Listagem de todos os cursos vinculados a cada faculdade.
8. Detalhamento da grade curricular completa por semestre/ano de cada curso.
9. Informar horários e turnos disponíveis (matutino, vespertino, noturno, integral, EAD).
10. Exibir a duração total de cada curso (semestres ou anos).
11. Apresentar a mensalidade base de cada curso.
12. Listar opções de bolsas privadas e descontos aplicáveis.
13. Sinalizar claramente se o curso é 100% gratuito.
14. Indicar se a instituição aceita inscrição via SISU.
15. Indicar se a instituição aceita o FIES.
16. Indicar se a instituição participa do ProUni.
17. Exibir calendário com datas dos próximos vestibulares e processos seletivos.
18. Exibir nota de corte aproximada para cada curso por modalidade de ingresso.
19. Permitir que faculdades sejam cadastradas e exibidas independentemente de adesão prévia.

## Módulo 2 – Cadastro e Perfil do Aluno
20. Cadastro de novos alunos via e‑mail e senha.
21. Login social (Google, Apple, Facebook).
22. Perfil editável (nome, foto, bio, cidade, curso de interesse).
23. Alteração de senha e recuperação de acesso.
24. Validação de autenticidade do e‑mail no cadastro.
25. Definir status acadêmico (Vestibulando, Matriculado, Ex‑aluno).
26. Vincular perfil a uma faculdade após matrícula.

## Módulo 3 – Busca, Filtros e Navegação
27. Barra de busca global por nome de faculdade, curso ou cidade.
28. Filtrar faculdades por faixa de preço da mensalidade.
29. Filtrar cursos por modalidade (Presencial, EAD, Semipresencial).
30. Filtrar por programas de incentivo (SISU, FIES, ProUni, Bolsa Própria).
31. Ordenar resultados por menor preço, melhor nota do MEC ou avaliação dos alunos.
32. Exibir sugestões de busca por termos mais procurados.
33. Comentários e avaliações de alunos e ex‑alunos sobre faculdades.
34. Calcular média das avaliações para exibição no card da faculdade.
35. Moderação ou denúncia de comentários impróprios.
36. Salvar faculdades na lista de "Objetivos" / Favoritos.
37. Exibir número total de alunos que salvaram a faculdade como objetivo.
38. Mostrar quais outros usuários salvaram a mesma faculdade.
39. Listar na Home os maiores e mais acessados sites/instituições da plataforma.
40. Carrossel ou grade com cursos em destaque e maiores descontos.
41. Seção na Home para depoimentos de alunos em destaque.
42. Atalho rápido na Home para busca filtrada por estado e cidade.

## Processo de Matrícula Integrada
- Iniciar e concluir matrícula diretamente na plataforma.
- Formulário para coleta de dados pessoais.
- Upload de documentos obrigatórios (RG, CPF, Histórico Escolar, Comprovante de Residência).
- Integração com gateway de pagamento para taxa de matrícula ou 1ª mensalidade.
- Gerar comprovante de pré‑matrícula em PDF.
- Notificar aluno sobre status da aprovação.
- Painel para a faculdade acompanhar matrículas recebidas.

## Módulo 7 – Portfólio de Projetos do Aluno
- Cadastro e publicação de projetos acadêmicos e pessoais.
- Upload de imagens, capas e arquivos anexos.
- Inserção de links externos (GitHub, Figma, YouTube, Behance).
- Marcar faculdade e curso onde o projeto foi desenvolvido.
- Tags de competências/tecnologias.
- Vitrine pública do portfólio para compartilhamento externo.
- Categorizar projetos (TCC, Artigo, Design, Software, Extensão).

## Módulo 8 – Repositório de Materiais de Aula
- Upload de materiais (resumos, apostilas, exercícios).
- Categorizar por disciplina, período e faculdade.
- Visualização prévia de documentos (PDF, imagens).
- Download pelos demais alunos.
- Busca por disciplinas e materiais acadêmicos.

## Módulo 9 – Rede Social e Networking
- Feed de notícias com atualizações de projetos e materiais.
- Seguir outros alunos e profissionais.
- Curtir, reagir e comentar projetos e materiais.
- Compartilhar projetos/portfólios em redes sociais externas.
- Empresas/recrutadores visualizam portfólios.
- Mensagens diretas (chat) entre alunos cadastrados.
- Destaque de projetos mais populares na página da faculdade.

## Módulo 10 – Notificações e Comunicação
- E‑mails de confirmação de cadastro e alteração de senha.
- Alertas por e‑mail/notificação sobre prazos de vestibular e bolsas.
- Notificar aluno quando seu projeto receber curtidas ou comentários.
- Notificar status da matrícula.

## Módulo 11 – Painel Administrativo e Métricas
- Total de visualizações por faculdade e curso.
- Relatório de conversão de cliques em intenções de matrícula.
- Aprovar, reprovar ou moderar projetos e materiais denunciados.
- Listar termos de busca mais pesquisados sem resultado.

## Módulo 12 – Requisitos Não Funcionais (Desempenho, Segurança e Arquitetura)
- Página inicial e buscas < 2 s.
- Totalmente responsivo (Mobile, Tablet, Desktop).
- HTTPS para criptografia em trânsito.
- Senhas armazenadas com bcrypt/Argon2.
- Escalabilidade para picos de acesso (ENEM/SISU).
- Índices otimizados no banco de dados.
- Compressão automática de imagens.
- SLA ≥ 99,5 %.
- Busca textual eficiente (Elasticsearch ou PostgreSQL Full‑Text).
- Acessibilidade WCAG.
- Limite configurável de upload (ex.: 20 MB).
- CDN para arquivos estáticos.
- API RESTful ou GraphQL.
- Logs de auditoria.
- Armazenamento escalável (AWS S3 ou equivalente).
- Sessões expiram após inatividade.
- Proteção contra SQL Injection, XSS, CSRF.
- SEO otimizado.
- Backup diário automático.
- Design System para consistência visual.
- Concurrency sem perda de performance.
- Escalabilidade horizontal.
- Rate limiting nas APIs.

## Regras de Acesso (Etapas da Plataforma)
1. **Vitrine pública das faculdades** – Acessível sem login.
2. **Vitrine de moradias** – Exibe anúncios, sem intermediação.
3. **Vagas de emprego** – Disponíveis para aluno logado, baseado no curso.

## Vitrine Pública das Faculdades (Complemento)
- Exibir imagens de eventos.
- Acesso sem login.

## Vitrine de Moradias Estudantis
- Cadastro e exibição de imóveis (república, pensionato, kitnet, etc.).
- Upload de fotos, vídeos, tour virtual.
- Detalhes estruturais, regras, composição de valor.
- Associação a faculdades e campi próximos.
- Aviso de isenção de responsabilidade.
- Busca geolocalizada com filtro por raio, preço, modalidade, pet‑friendly.
- Cálculo de tempo de deslocamento.

## Mercado de Trabalho Inteligente e Carreiras
- Mapeamento dinâmico por curso → tags de mercado.
- Filtragem de vagas por curso e sub‑áreas.
- Tipos de vagas (Estágio, Trainee, Júnior, Freelance, Remoto, etc.).
- Ordenação por proximidade da faculdade ou moradia.
- Candidatura usando portfólio Palmer.
- Integração B2B para empresas publicarem vagas.
- Integração com APIs externas de agregadores.
- Compatibilidade % entre vaga e perfil.
- Salvar vagas favoritas e alertas de novas vagas.
- Acompanhar status da candidatura.

---

*Esta documentação pode ser expandida com diagramas, exemplos de payloads de API e fluxos de usuário conforme o projeto evolui.*