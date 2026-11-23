# Nexo ISP — EliteSoft Integrator (front-end demo)

Aplicação estática inspirada no Integrator 6. Sem backend, banco de dados ou dependências de build.

## GitHub Pages

Para publicar o site, abra **Settings → Pages**, escolha **Deploy from a branch**, selecione **main** e a pasta **/(root)** e salve. O Pages publicará o arquivo `index.html` da raiz.

## Pré-visualização local

Os arquivos CSS e JavaScript são distribuídos em segmentos gzip. Para abrir localmente, inicie um servidor HTTP estático na pasta do projeto:

```bash
python -m http.server 8000
```

Acesse `http://localhost:8000`.

## Funcionalidades

- Início com indicadores no estilo da referência.
- Cabeçalho, menu lateral expansível, submenus e abas.
- Pesquisa, cadastro, edição e ficha detalhada de clientes.
- Oito clientes fictícios com planos e configurações variadas de rede e pagamento.
- Prospectos, atendimentos, ordens de serviço e agenda técnica.
- Pontos de acesso, Site Survey, central de mensagens, BI e gráfico de NAS.
- Financeiro, planejamento orçamentário e painel de autenticações.
- Filtros, operações locais, exportação CSV e persistência via `localStorage`.
- Animações e preferências de movimento.

## Arquivos

- `index.html` — estrutura e inicialização.
- `app.js.gz.part0` até `app.js.gz.part4` — lógica JavaScript em segmentos gzip.
- `styles.css.gz.part0` até `styles.css.gz.part2` — estilos em segmentos gzip.

O navegador junta e descomprime os segmentos localmente com `DecompressionStream`; é necessário um navegador moderno.

## Limitações

Somente front-end: não há API, backend, autenticação real, integração RADIUS/roteadores, cobrança ou pagamentos. Os dados são fictícios e ficam salvos no armazenamento do navegador. O aviso de certificado SSL foi removido.
