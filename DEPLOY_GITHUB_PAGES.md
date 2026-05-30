# Deploy Landing Page → GitHub Pages

## Antes de começar
- Ter uma conta no GitHub (github.com)
- Ter o Git instalado (git-scm.com/download/win)

---

## PASSO 1 — Criar o repositório no GitHub

1. Acesse https://github.com/new
2. Nome do repositório: `landing-siqueira`
3. Visibilidade: **Public**
4. **NÃO** marque nenhuma opção (sem README, sem .gitignore)
5. Clique em **Create repository**
6. Copie a URL que aparece (ex: `https://github.com/pablolessa05/landing-siqueira.git`)

---

## PASSO 2 — Abrir o CMD na pasta da Landing Page

1. Abra o Explorer e vá até:
   `C:\Users\WINDOWS 10\Documents\Claude\Projects\Siqueira Estrategia\Landind Page`
2. Clique na barra de endereço do Explorer
3. Digite `cmd` e pressione Enter
4. O CMD abrirá já dentro da pasta correta

---

## PASSO 3 — Inicializar e enviar ao GitHub

Cole esses comandos **um por vez** no CMD:

```
git init
git add .
git commit -m "Landing page Siqueira Estratégia"
git branch -M main
git remote add origin https://github.com/pablolessa05/landing-siqueira.git
git push -u origin main
```

> ⚠️ Substitua a URL pelo link copiado no Passo 1.
> O Git pode pedir seu usuário e senha (ou token) do GitHub na primeira vez.

---

## PASSO 4 — Ativar o GitHub Pages

1. No repositório criado, clique em **Settings**
2. No menu lateral, clique em **Pages**
3. Em "Branch", selecione **main** → pasta **(root)**
4. Clique em **Save**
5. Aguarde ~2 minutos

Seu site estará em:
👉 `https://pablolessa05.github.io/landing-siqueira/`

---

## PASSO 5 — Adicionar o Meta Pixel ID

Antes do deploy (ou depois de criar o Pixel no Gerenciador de Anúncios):

1. Abra o arquivo `index.html` com o Bloco de Notas
2. Use Ctrl+H (localizar e substituir)
3. Localizar: `SEU_PIXEL_ID`
4. Substituir por: seu ID real (ex: `1234567890`)
5. Salve e refaça o deploy com:

```
git add index.html
git commit -m "Adiciona Meta Pixel"
git push
```

---

## Atualizar o site no futuro

Sempre que modificar qualquer arquivo:

```
git add .
git commit -m "Descrição da atualização"
git push
```

O GitHub Pages atualiza automaticamente em ~1 minuto.
