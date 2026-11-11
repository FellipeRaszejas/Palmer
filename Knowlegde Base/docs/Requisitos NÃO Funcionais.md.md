# Requisitos Não Funcionais da Plataforma Palmer

## Performance
- **Tempo de carregamento**: a página inicial e as páginas de busca devem carregar em menos de **2 segundos**.
- **Busca por geolocalização de imóveis**: tempo de resposta < **1,5 segundo**.
- **Escalabilidade**: suportar picos de acesso durante períodos críticos (ex.: divulgação ENEM/SISU) sem degradação perceptível.
- **Cache/CDN**: utilização de CDN para servir arquivos estáticos (imagens, vídeos, PDFs) com latência mínima.

## Responsividade & UX
- Interface totalmente responsiva (Mobile, Tablet, Desktop).
- Design System com componentes reutilizáveis para consistência visual.
- Acessibilidade (WCAG): contraste adequado, navegação por teclado, suporte a leitores de tela.
- SEO otimizado para ranqueamento no Google.

## Segurança
- **HTTPS** obrigatório em todo o tráfego.
- **Armazenamento de senhas**: hash forte (bcrypt ou Argon2) com salt.
- **Proteção contra ataques web**: prevenção de SQL Injection, XSS, CSRF.
- **Rate limiting** nas APIs para evitar DDoS e abuso.
- **Logs de auditoria** para ações administrativas críticas.
- **Sessões**: expiração automática após período de inatividade.

## Confiabilidade & Disponibilidade
- **SLA**: disponibilidade mínima de **99,5 %**.
- **Backup**: backup automático diário dos bancos de dados.
- **Persistência de arquivos**: armazenamento em nuvem escalável (ex.: AWS S3 ou equivalente).
- **Monitoramento**: alertas para falhas de serviço e degradação de performance.

## Infraestrutura & Arquitetura
- **Arquitetura horizontalmente escalável** (autoscaling de instâncias de aplicação).
- **Banco de dados**: índices otimizados para consultas rápidas (cursos, faculdades, vagas).
- **Busca textual eficiente**: usar Elasticsearch ou PostgreSQL Full‑Text.
- **Compressão automática** de imagens enviadas nos projetos e galerias.
- **API**: estruturada no padrão **RESTful** ou **GraphQL**.
- **Controladores de taxa** (rate limiting) nas rotas públicas da API.

## Dados & Integrações
- **Limite de upload**: configurável, padrão **20 MB** por arquivo.
- **Geolocalização**: uso de coordenadas lat/long com **spatial indexing** para buscas rápidas.
- **Integrações externas**: APIs de agregadores de vagas, gateways de pagamento, serviços de email (SMTP/SendGrid).

---

*Esta seção deve ser complementada com métricas específicas, limites de carga e diagramas de arquitetura ao avançar o desenvolvimento.*