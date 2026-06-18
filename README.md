# Rede Social de Microblog

API REST de microblog com JWT, seguidores e timeline personalizada.

> 📦 **Template de trabalho em grupo da WebForge.** Clique em **Use this template** (botão verde acima) para criar o repositório do seu grupo.

## 🚀 Como rodar

```bash
npm install
npm start        # inicia em http://localhost:3000
```

O projeto já sobe com uma rota raiz `GET /`. Todo o resto é com o grupo.

## 📋 Requisitos

- **Auth/Perfil** — registro com @username **único**, login JWT, `GET /perfil/:username`, `PATCH /perfil`.
- **Posts** — `POST /posts` (texto até 280 caracteres), `GET /posts/:id`, `DELETE /posts/:id` (próprio).
- **Seguidores** — seguir/deixar de seguir e listar seguidores/seguindo.
- **Timeline/Interações** — `GET /timeline` (posts de quem o usuário segue, paginado), curtir/descurtir e comentar.

> Persistam os dados (arquivo JSON ou SQLite) — os testes podem reiniciar o servidor entre etapas.

## ✅ O que os testes de correção validam

Os testes automáticos sobem o **seu** servidor e fazem requisições HTTP reais contra a API. Eles verificam **comportamento** (status HTTP e corpo das respostas), não a estrutura interna do código — organizem os arquivos como preferirem. Para ser aprovado, a API precisa:

- [ ] `GET /` responde **200**.
- [ ] Registrar com um **@username já usado** responde **409** (ou 400).
- [ ] `POST /auth/login` retorna um token JWT.
- [ ] `POST /posts` com mais de **280 caracteres** responde **400**.
- [ ] Seguir um usuário passa a incluí-lo na contagem de seguidores.
- [ ] `GET /timeline` retorna **apenas** posts de usuários seguidos, sem duplicatas.
- [ ] Curtir o mesmo post duas vezes não conta dois likes.
- [ ] Rota protegida sem token responde **401**.

## 👥 Trabalho em equipe (obrigatório)

Este é um ambiente o mais próximo possível do mercado:

- O repositório deve pertencer a **um** dos membros do grupo. Os **demais membros entram como colaboradores** em `Settings → Collaborators → Add people`.
- Cada membro trabalha em sua **própria branch** e abre **Pull Request** para a `main`, pedindo revisão de outro colega.
- A WebForge mede as **contribuições individuais** de cada membro (commits, linhas adicionadas e removidas) direto do histórico do GitHub. Distribuam bem o trabalho.

## 🧱 Stack

- Node.js + Express (CommonJS)
