# Leads Polo Cruzeiro do Sul Virtual

Cópia do painel de leads da UniFECAF, começando do zero (sem leads, sem equipe) e com banco próprio.
Site estático (GitHub Pages) com dados no Firebase (Firestore) e login por e-mail e senha.

## Arquivos

- `index.html` — o painel inteiro.
- `config.js` — configuração do Firebase e e-mail da administradora.
- `firestore.rules` — quem pode ler e alterar os dados (já com o e-mail da administradora).
- `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` — instalar como aplicativo no celular.

## Configuração (uma vez)

1. **GitHub**: crie um repositório novo (ex.: `leadscruzeiro`) e suba todos estes arquivos.
2. **Firebase**: em console.firebase.google.com, crie um projeto NOVO (ex.: `leads-cruzeiro`) e adicione um app **Web**. Copie o `firebaseConfig` para `FIREBASE_CONFIG` no `config.js`.
3. **Login**: Authentication → Método de login → ative **E-mail/senha**. Em Usuários, crie o login da administradora.
4. **Banco**: Firestore Database → Criar banco → modo de produção → região `southamerica-east1 (São Paulo)`.
5. **Regras**: Firestore → Regras → cole o conteúdo de `firestore.rules` e clique em Publicar.
6. **Domínio**: Authentication → Configurações → Domínios autorizados → adicione `isabelladutras.github.io`.
7. **GitHub Pages**: Settings → Pages → Deploy from a branch → `main` / raiz.
8. **Cursos**: no painel, Configurações → Cursos oferecidos → ajuste para o catálogo do polo.

## Dia a dia

Igual ao painel UniFECAF: equipe na aba **Equipe**, backup mensal no Início, lixeira de 30 dias, duplicados em Configurações.
