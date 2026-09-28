# DopamineRun — app para iPhone (PWA)

Tarefas que viram tempo de jogo. Funciona offline, em tela cheia, sem App Store.

## Conteúdo do pacote
- `index.html` — o app
- `sw.js` — faz o app funcionar sem internet
- `manifest.webmanifest` e ícones — nome e ícone na tela de início
- `baloo2.woff2` — fonte (licença SIL OFL, ver `OFL.txt`)

## Publicar grátis no GitHub Pages (uma vez só, ~10 min, melhor pelo computador)
1. Crie uma conta em github.com (se ainda não tiver).
2. Clique em **New repository**. Nome: `dopaminerun`. Marque **Public**. Clique em **Create repository**.
3. Na página do repositório, clique em **uploading an existing file**.
4. Arraste **todos os arquivos desta pasta** (não a pasta em si) e clique em **Commit changes**.
5. Vá em **Settings → Pages**. Em *Branch*, escolha `main` e a pasta `/ (root)`. Clique em **Save**.
6. Em 1 a 2 minutos o endereço aparece no topo da página: `https://SEU-USUARIO.github.io/dopaminerun/`

O código do app fica público, mas seus dados não: moedas, tarefas e fotos ficam só no seu iPhone.

## Ranking com amigos (configurar uma vez no Supabase)
1. Entre em supabase.com e abra o seu projeto.
2. Vá em **Authentication → Sign In / Providers** e ative **Allow anonymous sign-ins**. Clique em **Save**.
   (Os nomes dos menus podem variar um pouco; procure por "anonymous".)
3. Vá em **SQL Editor → New query**, cole TODO o conteúdo do arquivo `supabase-ranking.sql` (no pacote do projeto, ele fica em `../supabase/`) e clique em **Run**.
   Deve aparecer "Success. No rows returned". Pode rodar de novo no futuro sem perder dados.
4. Envie os arquivos do app para o GitHub (o `supabase-ranking.sql` pode ir junto, não faz mal).

### Teste rápido depois de configurar
1. Abra o app pelo ícone → aba **Ranking** → escolha um apelido e um nome de liga → **Criar liga**.
2. Conclua uma tarefa, volte ao Ranking e toque em **Atualizar**: devem aparecer 10 pontos.
3. Toque em **Convidar amigos** e mande o convite. O amigo instala o app e entra com o código.

### Regras de pontos (calculadas pelo servidor)
- Tarefa concluída: 10 pontos, até 10 tarefas por dia.
- Meta diária batida: 20 pontos, uma vez por dia.
- O ranking zera toda segunda-feira (horário de Brasília).
- Só o apelido e os pontos vão para o servidor. Fotos e tarefas ficam no celular.

### Cuidados
- A chave `sb_publishable_...` fica no código de propósito: ela é pública. Quem protege os dados são as regras do script.
- Nunca coloque no app nem envie a ninguém a senha do banco nem a chave secreta (`sb_secret_...` ou `service_role`).
- Projetos gratuitos do Supabase pausam depois de 7 dias sem uso. Se o ranking parar, entre no painel e clique em **Restore**.

## Instalar no iPhone
1. Abra o endereço no **Safari**.
2. Toque em **Compartilhar** → **Adicionar à Tela de Início** → **Adicionar**.
3. Abra sempre pelo ícone da tela de início.

## Backup
Seus dados ficam só no iPhone. Em **Ajustes → Fazer backup**, salve o arquivo em **Arquivos** ou no **iCloud Drive**.
Para trocar de celular ou reinstalar: **Ajustes → Restaurar** e escolha o arquivo.
Se você remover o app da tela de início, os dados são apagados junto. Faça backup antes.

## Atualizar o app
Envie os arquivos novos para o mesmo repositório (substituindo os antigos).
A nova versão entra na segunda vez que você abrir o app. Seus dados não são afetados.

**Atualização 4.1 (iOS 26):** para acabar com o espaço vazio embaixo da barra de navegação, é preciso reinstalar o app uma única vez. O iOS só lê o estilo da barra de status na instalação.
1. Ajustes → **Fazer backup** (se já tiver dados).
2. Remova o app da Tela de Início e adicione de novo pelo Safari.
3. Ajustes → **Restaurar**. A conta do ranking precisa entrar de novo na liga.
