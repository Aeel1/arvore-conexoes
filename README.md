Árvore de Conexões
Descrição
Este projeto é um webapp de página única desenvolvido para criar uma visualização de árvore genealógica de conexões, projetado para uso por promotores. Ele permite mapear relações entre pessoas, inserindo nomes, dados pessoais (como CPF, profissão) e imagens, e criando conexões entre elas. O app possui uma interface profissional com layout otimizado, utilizando React para a interface, vis.js para renderizar o grafo interativo, Tailwind CSS para estilização e jsPDF para exportação em PDF. Anúncios do Google AdSense foram integrados nas barras laterais (esquerda e direita) e na parte inferior da página para gerar receita e manter o site online. Na primeira visita, o site carrega automaticamente um exemplo com 4 pessoas e 3 conexões. Os dados pessoais aparecem abaixo do nome no grafo, centralizados, com quebras de linha. As conexões são exibidas como linhas simples, sem setas.
Estrutura da Pasta

index.html: Contém o código principal do webapp, incluindo HTML, JavaScript (React), CSS (via Tailwind) e integração com Google AdSense.
sobre.html: Página com informações sobre o projeto, para melhorar a aprovação do AdSense.
README.md: Este arquivo de documentação.

Como Executar

Copie o conteúdo do arquivo index.html para um arquivo local com o mesmo nome.
Abra o arquivo index.html em um navegador web moderno (como Chrome, Firefox ou Edge).
Para hospedar online, use o GitHub Pages (veja instruções em "Hospedar no GitHub Pages").
Não é necessário configurar um servidor, pois o app utiliza CDNs para todas as dependências (React, vis.js, Tailwind CSS, jsPDF, Google AdSense).

Funcionalidades

Exemplo Automático: Na primeira visita, o site carrega um exemplo com 4 pessoas (João Silva, Maria Souza, Pedro Santos, Ana Oliveira) e 3 conexões (João - Maria, Maria - Pedro, Pedro - Ana), com posições fixas no grafo. Esse exemplo não sobrescreve projetos salvos anteriormente.
Exibição no Grafo: O nome de cada pessoa aparece no grafo com os dados pessoais abaixo, centralizados. Os dados pessoais são divididos em linhas (máximo de 30 caracteres por linha) para melhor legibilidade.
Conexões sem Setas: As conexões entre pessoas são exibidas como linhas simples, sem setas, conectando os nós no grafo.
Adicionar Pessoa: Insira nome, dados pessoais e uma imagem (opcional, via upload ou copiar/colar). A imagem é exibida em uma visualização prévia com opção de remoção.
Editar Pessoa: Edite os dados de uma pessoa existente usando a lista de pessoas.
Remover Pessoa: Remova uma pessoa e suas conexões associadas, com confirmação antes da exclusão.
Adicionar Conexão: Crie conexões entre pessoas selecionando uma origem e um destino.
Remover Conexão: Remova conexões existentes, com confirmação antes da exclusão.
Novo Projeto: Crie um novo projeto, limpando todos os dados atuais, com confirmação antes da ação. Após limpar, o exemplo automático não é recarregado até que o localStorage seja limpo.
Visualização Interativa: Um grafo interativo exibe as conexões, com suporte a arrastar nós individualmente (sem mover outros nós), zoom e tooltips com detalhes. As posições dos nós são persistidas.
Exportação: Exporte o grafo como imagem PNG ou PDF usando botões com ícones.
Salvar/Carregar Projeto: Salve as pessoas, conexões e posições dos nós como um arquivo JSON (no formato <nome-do-projeto>-conexoes.json) para reutilização e carregue um arquivo JSON salvo anteriormente.
Interface Profissional: Layout otimizado com paleta de cores sóbria, botões estilizados e listas expansíveis/recolhíveis para conexões e pessoas. A lista de conexões inicia oculta por padrão.
Persistência: Os dados, incluindo posições dos nós, são salvos no localStorage do navegador, persistindo enquanto o cache não for limpo.
Monetização com Google AdSense: Anúncios display responsivos são exibidos nas barras laterais (esquerda e direita) e na parte inferior da página para gerar receita.

Como Usar

Configurar Google AdSense (para monetização):
Crie uma conta no Google AdSense (https://www.google.com/adsense) e aguarde a aprovação do site.
Após aprovação, obtenha o código de anúncio no painel do AdSense (em "Anúncios" > "Por unidade de anúncio" > "Anúncios de display").
Substitua o ca-pub-XXXXXXXXXXXXXXXX no index.html pelo seu client-id real.
Crie unidades de anúncio para as posições "Barra Lateral Esquerda", "Barra Lateral Direita" e "Banner Inferior", e atualize os data-ad-slot no index.html com os IDs fornecidos pelo AdSense.
O script de inicialização no index.html evita erros como Uncaught TagError: adsbygoogle.push().


Hospedar no GitHub Pages:
Clone o repositório:git clone https://github.com/seu-usuario/arvore-conexoes.git
cd arvore-conexoes


Adicione os arquivos index.html, sobre.html e README.md:git add index.html sobre.html README.md
git commit -m "Remove setas das conexões no grafo"
git push origin main


Configure o GitHub Pages:
No GitHub, vá para o repositório > "Settings" > "Pages".
Em "Source", selecione o ramo main e a pasta / (root).
Salve e aguarde a publicação (pode levar alguns minutos).
Acesse o site em https://seu-usuario.github.io/arvore-conexoes.




Explorar o Exemplo Automático:
Na primeira visita, o grafo exibirá 4 pessoas (João Silva, Maria Souza, Pedro Santos, Ana Oliveira) conectadas em sequência (João - Maria - Pedro - Ana).
Cada nó mostra o nome da pessoa com os dados pessoais abaixo, centralizados, com quebras de linha (ex.: "Advogado,\nCPF 123.456.789-00").
As conexões são linhas simples, sem setas, ligando os nós.
Passe o mouse sobre um nó para ver o tooltip com detalhes (nome, dados pessoais, imagem, se houver).
A lista de pessoas e conexões estará visível nas seções expansíveis.
Para começar do zero, clique no botão "Novo Projeto" no canto superior direito.


Criar ou Limpar Projeto:
No painel "Rede de Conexões", clique no botão com ícone de documento ("Novo Projeto") para criar um novo projeto.
Confirme no alerta para limpar todos os dados atuais (pessoas, conexões, formulários, visualização de imagem).


Visualizar Rede de Conexões:
A rede de conexões aparece como um grafo interativo no topo da página, com anúncios nas laterais e inferior.
Cada nó exibe o nome da pessoa e, abaixo, os dados pessoais centralizados com quebras de linha.
As conexões entre nós são linhas retas sem setas.
Passe o mouse sobre um nó para ver detalhes adicionais no tooltip (nome, dados pessoais, imagem).
Arraste um nó para movê-lo sem afetar a posição dos outros nós; apenas as linhas conectadas a ele se ajustarão.
Use o zoom para navegar no grafo.
Abaixo do grafo, use os botões para:
Clicar no ícone de imagem (tooltip: "Exportar como PNG") para baixar o grafo como imagem.
Clicar no ícone de PDF (tooltip: "Exportar como PDF") para baixar o grafo como documento PDF.
Clicar em "Salvar Projeto" para salvar o projeto como um arquivo JSON. Você será solicitado a inserir o nome do projeto, e o arquivo será baixado como <nome-do-projeto>-conexoes.json.
Clicar em "Carregar Projeto" para selecionar um arquivo JSON salvo anteriormente e restaurar o projeto, incluindo as posições dos nós.




Adicionar Pessoa:
Preencha o campo "Nome".
Insira informações no campo "Dados Pessoais" (ex.: CPF, profissão). No grafo, o texto será dividido em linhas de até 30 caracteres.
Faça upload de uma imagem (opcional) clicando no input de arquivo ou pressione Ctrl+V para colar uma imagem copiada.
A imagem será exibida em uma visualização prévia abaixo do input de arquivo. Clique em "Remover" para limpar a imagem, se desejar.
Clique em "Adicionar Pessoa".


Gerenciar Conexões:
Para adicionar, selecione duas pessoas diferentes nos menus suspensos e clique em "Adicionar Conexão". A conexão aparecerá como uma linha sem seta no grafo.
Para visualizar ou remover, clique em "Expandir Conexões" para mostrar a lista de "Conexões Existentes" (a lista inicia oculta por padrão).
Na lista, clique no botão "Remover" ao lado de uma conexão e confirme no alerta.
Clique em "Recolher Conexões" para ocultar a lista novamente.


Gerenciar Pessoas Adicionadas:
Clique em "Expandir Pessoas" (ou "Recolher Pessoas" para ocultar) para mostrar a lista de "Pessoas Adicionadas" (inicia expanso por padrão).
Clique no botão "Editar" ao lado de uma pessoa para modificar seus dados; os campos do formulário e a visualização prévia da imagem serão preenchidos. Clique em "Salvar Alterações" ou "Cancelar Edição".
Clique no botão "Remover" ao lado de uma pessoa e confirme a



