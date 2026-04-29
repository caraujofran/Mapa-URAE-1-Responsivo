# Mapa Consolidado · Contratos 1 e 2

Página web interativa, totalmente responsiva, que exibe num único mapa todos os municípios, sedes de fiscalização, supervisão, gerenciamento e coordenação dos Contratos 1 (São Paulo) e 2 (São José dos Campos), com as ligações entre cada nível hierárquico.

## Funcionalidades

- **Mapa de fundo OpenStreetMap** com zoom contínuo (pinch-to-zoom no celular, scroll do mouse no desktop, botões `+` / `−`).
- **Camadas ligáveis e desligáveis** individualmente:
  - Municípios abrangidos
  - Sedes de fiscalização, supervisão, gerenciamento e coordenação
  - Ligações município → fiscalização → supervisão → gerenciamento → coordenação
- **Botões de contrato inteiro** (C1 e C2) que ligam ou desligam tudo do contrato de uma só vez.
- **Interface adaptativa**: layout completo no desktop (com painel de coordenações e controle Leaflet de camadas); barra superior, gaveta inferior e botão flutuante de legenda no celular.
- **Compatibilidade ampla**: Chrome, Safari, Edge, Firefox, Opera, Samsung Internet, Brave, em iOS e Android.

## Como acessar

Após publicar este repositório no GitHub Pages, o link ficará disponível em:

```
https://SEU-USUARIO.github.io/NOME-DO-REPO/
```

Basta abrir o link em qualquer navegador, no celular ou computador.

## Como publicar no GitHub Pages

1. **Crie um repositório no GitHub**
   Acesse [github.com/new](https://github.com/new), dê um nome (ex.: `mapa-contratos`) e marque como **Public**. Clique em *Create repository*.

2. **Suba os arquivos**
   Na página do repositório recém-criado, clique em *uploading an existing file* (ou em *Add file → Upload files*) e arraste para lá:
   - `index.html`
   - `.nojekyll`
   - `README.md`

   Em seguida clique em *Commit changes*.

3. **Ative o GitHub Pages**
   No repositório, vá em **Settings → Pages**.
   Em *Source*, selecione **Deploy from a branch**.
   Em *Branch*, selecione **main** e a pasta **/ (root)**. Clique em *Save*.

4. **Aguarde 1–3 minutos**
   O GitHub gera o link e mostra na própria tela de Pages. O endereço terá a forma `https://seu-usuario.github.io/nome-do-repo/`.

Pronto — o link já pode ser compartilhado e abre direto no navegador padrão de qualquer celular.

## Estrutura dos arquivos

| Arquivo       | Função                                                                 |
|---------------|------------------------------------------------------------------------|
| `index.html`  | Página principal com o mapa interativo. É a página servida na raiz.    |
| `.nojekyll`   | Arquivo vazio que desativa o processador Jekyll do GitHub Pages.       |
| `README.md`   | Esta documentação, exibida na página inicial do repositório no GitHub. |

## Detalhes técnicos

- HTML estático autocontido — toda a lógica está em `index.html`.
- Bibliotecas carregadas via CDN HTTPS (Leaflet 1.9.3, jQuery 3.7.1, Bootstrap 5.2.2, Font Awesome 6.2, Leaflet.awesome-markers).
- Sem backend, sem build, sem dependências locais.
- Suporte a `safe-area-inset` para iPhones com notch / Dynamic Island e Androids com barra de gestos.
- A interface mobile aparece automaticamente em telas com largura ≤ 900 px; acima disso, a interface desktop é preservada.

## Atualizando o conteúdo

Para alterar o mapa no futuro, basta substituir o `index.html` no repositório (botão *Add file → Upload files*, sobrescrevendo). O GitHub Pages republica em poucos minutos, automaticamente.
