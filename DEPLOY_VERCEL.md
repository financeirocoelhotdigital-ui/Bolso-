# 🚀 Como Subir o Bolso+ na Vercel

Os arquivos do projeto já estão **100% configurados e prontos** para deploy direto na Vercel com suporte completo para a aplicação React/Vite (Frontend SPA) e as funções de API/IA (Backend Serverless).

---

## 📁 Arquivos de Configuração Inclusos
1. **`vercel.json`**: Configura o build do Vite, a pasta `dist` e o roteamento automático do `/api/*` e do SPA.
2. **`api/index.ts`**: Ponto de entrada das funções serverless da Vercel (Gemini AI, gestão de usuários, comunicados e relatórios).
3. **`server.ts`**: Compatibilizado tanto para rodar localmente quanto na Vercel sem conflito de portas ou leitura de arquivos somente leitura.
4. **`.env.example`**: Lista de variáveis de ambiente necessárias.

---

## 🛠️ Passo a Passo para o Deploy

### Opção 1: Conectando com GitHub (Recomendado)
1. Suba o código do projeto para um repositório no seu **GitHub** (pode ser público ou privado).
2. Acesse [vercel.com](https://vercel.com) e faça login.
3. Clique em **"Add New..."** ➔ **"Project"**.
4. Importe o repositório do seu GitHub.
5. Em **Framework Preset**, a Vercel detectará automaticamente **Vite**.
6. Em **Environment Variables (Variáveis de Ambiente)**, adicione:
   - `GEMINI_API_KEY`: Sua chave de API do Google Gemini (para as funções de IA).
   - `ADMIN_EMAIL`: `dicasdereceitas1993@gmail.com`
7. Clique em **Deploy**! Em menos de 1 minuto seu app estará no ar com link `https://seu-projeto.vercel.app`.

---

### Opção 2: Pelo Terminal via Vercel CLI
Se preferir subir direto pelo terminal da sua máquina:
```bash
# 1. Instale a Vercel CLI (caso ainda não tenha)
npm install -g vercel

# 2. Faça login na sua conta Vercel
vercel login

# 3. Na raiz do projeto, execute o comando de deploy:
vercel --prod
```

---

## ⚠️ Passo Importante no Firebase (Login com Google & Autenticação)
Para que o login com Google e o Firebase Auth funcionem no domínio da Vercel:
1. Acesse o [Console do Firebase](https://console.firebase.google.com/).
2. Selecione o projeto `gen-lang-client-0297514368`.
3. Vá em **Authentication** ➔ aba **Settings (Configurações)** ➔ **Authorized domains (Domínios autorizados)**.
4. Clique em **Add domain** e adicione o seu domínio da Vercel (ex: `seu-projeto.vercel.app`).
5. Salve. Pronto! O login com Google e e-mail funcionará perfeitamente.
