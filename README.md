# Gerador de Assinatura de E-mail — GLP Laboratórios

Ferramenta web para os colaboradores da GLP Laboratórios gerarem sua própria assinatura de e-mail em PNG, preenchendo nome, cargo, telefone, WhatsApp, e-mail, local de atuação e foto.

Não precisa de backend nem banco de dados: é um único arquivo HTML que roda inteiramente no navegador. A foto enviada pela pessoa nunca sai do computador dela — tudo é processado localmente e o PNG final é gerado e baixado direto pelo navegador.

## Como subir este repositório no GitHub

1. Crie um repositório novo no GitHub (pode ser público ou privado — privado funciona normalmente com GitHub Pages em contas Pro/Team/Enterprise; em conta gratuita o Pages só funciona com repositório público).
2. Envie os arquivos desta pasta (`index.html` e este `README.md`) para o repositório. Pode ser pelo site do GitHub (botão "Add file" → "Upload files") ou por linha de comando:

   ```bash
   git init
   git add index.html README.md
   git commit -m "Gerador de assinatura de e-mail GLP"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   git push -u origin main
   ```

## Como publicar com um link público (GitHub Pages)

Se quiser um link tipo `https://seu-usuario.github.io/seu-repositorio/` para compartilhar com a equipe, sem precisar de hospedagem própria:

1. No repositório, vá em **Settings** → **Pages**.
2. Em "Build and deployment", escolha **Deploy from a branch**.
3. Selecione a branch **main** e a pasta **/ (root)**, depois clique em **Save**.
4. Em alguns minutos o GitHub mostra o link público na mesma tela (algo como `https://seu-usuario.github.io/nome-do-repo/`).

Como o arquivo se chama `index.html`, o link já abre a ferramenta diretamente, sem precisar digitar o nome do arquivo no final da URL.

## Como usar seu próprio domínio (opcional)

Se preferir usar um domínio próprio (ex: `assinatura.glplaboratorios.com.br`) em vez do link `github.io`:

1. No seu provedor de domínio, crie um registro CNAME apontando o subdomínio desejado para `seu-usuario.github.io`.
2. No repositório, em **Settings** → **Pages**, no campo "Custom domain", digite o domínio escolhido e salve.
3. Marque a opção **Enforce HTTPS** assim que ela ficar disponível (pode levar alguns minutos após configurar o domínio).

## Atualizando a ferramenta no futuro

Qualquer alteração (mudar cores, campos, layout, corrigir algo) é feita substituindo o conteúdo do arquivo `index.html` por uma nova versão e enviando (`git add` + `git commit` + `git push`) — o link de acesso continua o mesmo, e o GitHub Pages atualiza automaticamente em poucos minutos.

## Observações

- A ferramenta carrega a fonte "Sora" do Google Fonts, então quem for usá-la precisa estar com internet ativa no momento de preencher.
- Testado em Chrome, Edge e Firefox. Em iPhone/Safari, o download da imagem pode abrir em uma nova aba em vez de baixar direto — nesse caso, é só segurar a imagem e escolher "Salvar na galeria".
- Não há login nem controle de acesso: qualquer pessoa com o link pode gerar uma assinatura. Se isso for uma preocupação, é possível restringir o repositório/Pages ou colocar autenticação simples depois.
