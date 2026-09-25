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
