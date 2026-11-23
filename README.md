# Nexo ISP — EliteSoft Integrator (front-end demo)

Aplicação estática inspirada no Integrator 6. O repositório está preparado para hospedagem pelo GitHub Pages.

## Publicação no GitHub Pages

1. Abra **Settings → Pages** neste repositório.
2. Em **Build and deployment**, escolha **Deploy from a branch**.
3. Selecione a branch `main` e a pasta `/ (root)` e salve.
4. Aguarde o GitHub publicar o site.

## Pré-visualização local

Como os arquivos de estilo e lógica são servidos como recursos gzip estáticos, execute um servidor HTTP estático na pasta do projeto (não é backend):

```bash
python -m http.server 8000
```

Acesse `http://localhost:8000`.

## Funcionalidades

- Tela inicial com indicadores no padrão visual de referência.
- Cabeçalho, menu lateral expansível, submenus e abas.
- Pesquisa, cadastro, edição e ficha detalhada de clientes.
- Oito clientes fictícios com planos, autenticação, IP, VLAN, roteador, NAS e pagamento variados.
- Prospectos, atendimentos, ordens de serviço e agenda técnica.
- Pontos de acesso, Site Survey, central de mensagens, BI e gráfico de NAS.
- Financeiro, planejamento orçamentário e painel de autenticações.
- Filtros, operações locais, exportação CSV e persistência por `localStorage`.
- Animações e preferências de movimento.

## Arquivos

- `index.html` — estrutura e inicialização do aplicativo.
- `styles.css.gz` — estilos comprimidos em gzip para distribuição estática.
- `app.js.gz` — lógica JavaScript comprimida em gzip.

O navegador descomprime os dois recursos localmente. Requer navegador moderno com `DecompressionStream`.

## Limitações

Somente front-end: sem API, backend, autenticação real, RADIUS, roteadores, cobrança ou pagamentos. Dados fictícios salvos no navegador. A faixa de aviso de certificado SSL foi removida.