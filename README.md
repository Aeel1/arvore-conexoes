# Árvore de Conexões - rev0

## Descrição
Este projeto é um webapp de página única desenvolvido para criar uma visualização de árvore genealógica de conexões. Ele permite que promotores mapeiem relações entre pessoas, inserindo nomes, dados pessoais (como CPF, profissão) e imagens, e criando conexões entre elas. O app utiliza React para a interface, vis.js para renderizar o grafo interativo, Tailwind CSS para estilização e jsPDF para exportação em PDF.

## Estrutura da Pasta
- `index.html`: Contém o código principal do webapp, incluindo HTML, JavaScript (React) e CSS (via Tailwind).
- `README.md`: Este arquivo de documentação.

## Como Executar
1. Copie o conteúdo do arquivo `index.html` para um arquivo local com o mesmo nome.
2. Abra o arquivo `index.html` em um navegador web moderno (como Chrome, Firefox ou Edge).
3. Não é necessário configurar um servidor, pois o app utiliza CDNs para todas as dependências (React, vis.js, Tailwind CSS, jsPDF).

## Funcionalidades
- **Adicionar Pessoa**: Insira nome, dados pessoais e uma imagem (opcional) para registrar uma pessoa.
- **Adicionar Conexão**: Crie conexões entre pessoas selecionando uma origem e um destino.
- **Visualização Interativa**: Um grafo interativo exibe as conexões, com suporte a arrastar nós, zoom e tooltips com detalhes.
- **Exportação**: Exporte o grafo como imagem PNG ou PDF usando os botões fornecidos.
- **Persistência**: Os dados são salvos no `localStorage` do navegador, persistindo enquanto o cache não for limpo.

## Como Usar
1. **Adicionar Pessoa**:
   - Preencha o campo "Nome".
   - Insira informações no campo "Dados Pessoais" (ex.: CPF, profissão).
   - Faça upload de uma imagem (opcional).
   - Clique em "Adicionar Pessoa".
2. **Adicionar Conexão**:
   - Selecione duas pessoas diferentes nos menus suspensos.
   - Clique em "Adicionar Conexão".
3. **Visualizar Rede**:
   - A rede de conexões aparece como um grafo interativo.
   - Passe o mouse sobre um nó para ver detalhes.
   - Arraste nós ou use o zoom para navegar.
4. **Exportar Grafo**:
   - Clique em "Exportar como PNG" para baixar o grafo como imagem.
   - Clique em "Exportar como PDF" para baixar o grafo como documento PDF.

## Tecnologias Utilizadas
- **React 18.2.0**: Para a interface dinâmica.
- **vis.js 4.21.0**: Para renderização do grafo.
- **Tailwind CSS**: Para estilização responsiva.
- **jsPDF 2.5.1**: Para exportação do grafo como PDF.
- **Babel**: Para transpilar JSX.

## Limitações
- As imagens são convertidas para base64, então evite imagens muito grandes para não impactar o desempenho.
- Os dados são armazenados no `localStorage`, o que limita a persistência ao navegador do usuário.
- A exportação em PDF pode ter qualidade limitada para grafos muito grandes; ajustes manuais no layout podem ser necessários antes da exportação.
- Para uso em produção, considere adicionar um backend para armazenar dados e imagens.

## Próximos Passos
- Implementar edição e remoção de pessoas/conexões.
- Adicionar campos personalizados para dados pessoais.
- Melhorar a qualidade da exportação em PDF para grafos complexos.

## Autor
Desenvolvido por AeeL, em 22 de maio de 2025.