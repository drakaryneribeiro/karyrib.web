# Site — Dra. Karyne Ribeiro
## Instruções de Hospedagem

### Estrutura de arquivos
```
dra-karyne-site/
├── index.html        ← página principal
├── robots.txt        ← SEO: permite indexação
├── sitemap.xml       ← SEO: mapa do site
├── .htaccess         ← configurações Apache (Hostinger, Locaweb, etc.)
└── images/           ← todas as fotos e logos (formato .webp)
    ├── IMG_1905.webp
    ├── IMG_1907.webp
    ├── karyne-_13_of_69_.webp
    ├── karyne-_20_of_69_.webp
    ├── karyne-_28_of_69_.webp
    ├── karyne-_40_of_69_.webp
    └── karyne-_51_of_69_.webp
```

---

### Como publicar

#### Hostinger / Locaweb / Hostgator (cPanel)
1. Acesse o **Gerenciador de Arquivos** no painel
2. Navegue até a pasta `public_html`
3. Faça upload de **todos os arquivos e da pasta `images/`**
4. Certifique-se que `index.html` está na raiz de `public_html`
5. Pronto — acesse pelo seu domínio

#### Netlify (gratuito e rápido)
1. Acesse https://netlify.com e crie uma conta
2. Arraste a pasta `dra-karyne-site` inteira para o painel
3. O site vai ao ar instantaneamente com URL automática
4. Configure seu domínio personalizado em **Domain Settings**

#### Vercel (gratuito)
1. Acesse https://vercel.com
2. Faça upload ou conecte via GitHub
3. Configure domínio personalizado no painel

#### GitHub Pages (gratuito) — host escolhido
1. Crie um repositório no GitHub e suba todos os arquivos (com a pasta `images/`)
2. No repositório: **Settings → Pages**
3. Em **Source**, selecione a branch `main` e a pasta `/ (root)` → **Save**
4. Aguarde ~1 min; o site fica em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`
5. Para domínio próprio, veja a seção "Domínio personalizado" abaixo

> Observação: o arquivo `.htaccess` **não funciona** no GitHub Pages (é só para servidores Apache, como Hostinger). No GitHub Pages o HTTPS é ativado por uma caixinha em Settings → Pages ("Enforce HTTPS"). Pode manter o `.htaccess` no repositório — ele é simplesmente ignorado.

---

### Domínio personalizado no GitHub Pages
1. Em **Settings → Pages → Custom domain**, digite seu domínio (ex.: `drakaryneribeiro.com.br`) e salve. Isso cria um arquivo `CNAME` no repositório.
2. No painel do seu registrador de domínio (Registro.br, GoDaddy, etc.), crie os registros DNS:
   - **Domínio sem www** (apex): 4 registros `A` apontando para os IPs do GitHub:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - **www**: um registro `CNAME` apontando para `SEU-USUARIO.github.io`
3. Volte em Settings → Pages e marque **Enforce HTTPS** (pode levar até 24h para liberar o certificado).

---

### Após publicar — atualize estes arquivos
Troque `SEU-DOMINIO.com.br` pelo seu domínio real em:

- **index.html** — tags `canonical`, `og:url`, `og:image`, `twitter:image` (no topo do arquivo)
- **sitemap.xml** — a tag `<loc>`
- **robots.txt** — a linha `Sitemap:`

---

### SSL / HTTPS
- Hostinger, Netlify e Vercel oferecem SSL gratuito (Let's Encrypt)
- Ative nas configurações do painel para garantir o cadeado 🔒

---

### WhatsApp
O número configurado é: **(85) 98569-6333**
Link direto: https://wa.me/5585985696333

### Instagram
Perfil vinculado: **@drakaryneribeiro**
Link: https://www.instagram.com/drakaryneribeiro
