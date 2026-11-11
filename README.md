# Pokémon Circuit Randomizer — GitHub Pages

Pacote pronto para publicar. O jogo e o emulador estão incluídos; não é necessário selecionar ROM nem importar um save inicial. O primeiro carregamento transfere cerca de 66 MB de ROM compactada, mais os demais arquivos.

## Publicar pelo navegador

1. Extraia este ZIP no seu computador. Não envie o ZIP ao repositório.
2. Abra seu repositório no GitHub e escolha **Add file → Upload files**.
3. Arraste **todos os arquivos e pastas extraídos** para a tela de upload. O arquivo **index.html deve ficar na raiz do repositório**, ao lado de player.html, player.js e das pastas engine/ e rom/. Não coloque uma pasta extra envolvendo esses arquivos.
4. Inclua também os arquivos `.nojekyll` e `.gitattributes`. Se o seu gerenciador esconder arquivos que começam com ponto, habilite a exibição ou crie `.nojekyll` pelo GitHub em Add file → Create new file; basta uma linha vazia.
5. Finalize em **Commit changes** na branch `main` (ou na branch principal do seu repositório).
6. Abra **Settings → Pages**.
7. Em **Source**, escolha **Deploy from a branch**. Selecione **main** e **/(root)** e clique em **Save**.
8. Aguarde a publicação e use o endereço mostrado em **Visit site**. O processo pode levar alguns minutos; consulte a aba Actions se houver falha.

Se você usa o plano gratuito, utilize um repositório público para o Pages. O site publicado é acessível pela internet.

## Como conferir a estrutura

Na raiz devem aparecer index.html, player.html, player.js, README.md, .nojekyll e as pastas engine/, rom/ e assets/. O ZIP não tem uma pasta externa para que você possa adicionar seu conteúdo diretamente na raiz.

A pasta rom/ contém manifest.json e cinco arquivos circuit-00.bin a circuit-04.bin. São partes compactadas da ROM, e não devem ser renomeadas, removidas nem substituídas por ponteiros Git LFS. Cada parte tem no máximo 16 MB. Todos os caminhos são relativos e funcionam em um endereço de projeto, como https://SEU-USUARIO.github.io/SEU-REPOSITORIO/.

Não é preciso Node.js, npm, compilação, servidor Oracle ou backend para publicar este pacote. Mantenha engine/desmond.wasm junto dos arquivos JavaScript. Abra pelo endereço HTTPS do Pages; dar dois cliques no index.html local pode impedir o carregamento dos arquivos.

## Compartilhamento e progresso

Envie aos colegas o link do Pages. O botão Baixar página HTML gera um acesso que aponta para o endereço onde a página está publicada, incluindo o nome do repositório. Esse HTML baixado requer internet; não contém sozinho o jogo inteiro.

O progresso fica no navegador de cada jogador. Baixar progresso .sav exporta um backup de 512 KB. Alterar o domínio, navegador ou dispositivo não transfere o progresso automaticamente. Exporte antes de mudar de endereço ou limpar os dados do navegador. O jogo retoma o checkpoint da run, não o turno em andamento.

## Validação e limites

A integração original foi validada no Chrome remoto com vitória contra Brock, prêmio de 1400, cura dos seis Pokémon, ovo pendente, exportação de save e retomada da mesma equipe após reabrir. Este pacote conserva essa ROM e esse núcleo; foram ajustados apenas a apresentação de compartilhamento e o endereço do HTML exportado para o GitHub Pages.

Não foi testada uma campanha completa nem a importação pela interface, o áudio ou celulares. O erro relatado no DeSmuME Windows permanece separado do funcionamento no navegador. VALIDACAO.json registra os testes anteriores. O endereço do seu repositório não foi informado, portanto este pacote foi preparado para ser portátil e ainda não foi publicado/testado no seu GitHub Pages.

## Créditos

Veja engine/LEIA-ME.txt e engine/GPL-2.0.txt para créditos, licença e referências de código-fonte. Os créditos de sprites e do emulador também aparecem no rodapé do site. Os arquivos incluídos conservam os créditos do projeto original.
