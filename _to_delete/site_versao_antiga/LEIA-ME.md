# Site InfraCtrl — HTML estático

Site de apresentação completo, no visual da marca (fundo `#0d0d0d`, verde `#2ECC71`, Inter + JetBrains Mono).

## Estrutura
```
index.html                        Home (refeita, com prova social)
cases.html                        Cases de sucesso (listagem)
case-devlith.html                 Estudo de caso modelo
sobre.html                        Institucional / quem somos
seguranca.html                    Segurança & Compliance (LGPD)
artigos.html                      Hub de artigos
artigo-sql-server-bloqueios.html  Artigo completo (modelo)
assets/styles.css                 Design system compartilhado
robots.txt · sitemap.xml          SEO técnico
```

## Como publicar
É HTML/CSS puro, sem build. Basta subir a pasta inteira em qualquer hospedagem estática:
- **Vercel / Netlify:** arraste a pasta ou conecte o repositório. As URLs "limpas" (/cases) funcionam automaticamente.
- **Seu servidor atual / S3:** suba os arquivos mantendo a pasta `assets/` junto.

Depois de publicar, envie o `sitemap.xml` no Google Search Console e no Bing Webmaster.

## O QUE VOCÊ PRECISA TROCAR ANTES DE PUBLICAR
1. **Número de WhatsApp** — em `index.html`, variável `WHATSAPP` no `<script>` (formato internacional, só dígitos).
2. **Números e depoimentos dos cases** — `cases.html` e `case-devlith.html` estão com dados ILUSTRATIVOS. Troque pelos reais e valide o depoimento com o cliente.
3. **Página Sobre** — preencha o parágrafo entre `[colchetes]` (ano de fundação, cidade, time).
4. **Página Segurança** — revise as afirmações de conformidade com seu jurídico.
5. **E-mail de contato** — `contato@infractrl.com.br` (ajuste se for outro).
6. **og-image.png** — crie uma imagem 1200×630 e coloque na raiz (as meta tags já apontam para ela).
7. **Logo** — o cabeçalho usa a versão melhorada em texto (infra branco / ctrl verde). Se quiser trocar por imagem, gere um SVG (ver relatório estratégico).

## Observação sobre URLs
As tags canônicas e o sitemap usam os nomes de arquivo `.html` para funcionar em qualquer host. Se você configurar URLs limpas (sem `.html`), atualize os `<link rel="canonical">`, os `og:url` e o `sitemap.xml` para as versões sem extensão.
