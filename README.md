# LabTest — Laboratório didático de Testes de Software

## Arquivos
- `index.html`: site público dos alunos, sem o gabarito.
- `gabarito-professor.html`: gabarito local reservado ao professor. **Não envie este arquivo ao GitHub Pages público**.

## Testar localmente
1. Extraia o ZIP.
2. Abra `index.html` em um navegador atualizado.
3. Abra `gabarito-professor.html` localmente para consultar as respostas; não publique esse arquivo.
4. No site, cada aluno deve preencher nome completo e turma antes de começar.
5. Resultados, observações e defeitos são salvos automaticamente no armazenamento local do navegador (`localStorage`), separados pela identificação nome + turma.
6. Na tela “Finalizar atividade”, clique em “Finalizar e baixar relatório HTML” para gerar o único arquivo de entrega.

## Publicar gratuitamente com GitHub Pages
1. Entre em https://github.com e crie um repositório novo, por exemplo `labtest-senai`. Deixe-o **Public**.
2. Envie **somente `index.html`** para o repositório. Não envie `gabarito-professor.html`.
3. Abra **Settings > Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Em **Branch**, selecione `main` e a pasta `/(root)`. Clique em **Save**.
6. Aguarde a publicação. A página mostrará a URL pública, normalmente `https://SEU-USUARIO.github.io/labtest-senai/`.
7. Teste a URL em janela anônima e em um celular antes de compartilhar com a turma.

## Casos de teste
- O laboratório contém 12 casos: oito iniciais e quatro adicionais para variações de busca, validação de quantidade e persistência dos registros.
- O arquivo principal de entrega é o relatório final HTML, gerado na tela “Finalizar atividade”. Somente o botão “Finalizar e baixar relatório HTML” gera o arquivo para entrega; os botões de exportação CSV foram removidos para evitar confusão.

## Como funciona o salvamento
- O sistema salva os resultados, observações e defeitos automaticamente no navegador.
- Isso **não é um banco de dados central**: os dados ficam apenas no navegador/dispositivo onde foram preenchidos.
- Se o aluno mudar de computador/navegador, usar navegação privada ou limpar os dados do navegador, os registros locais não estarão disponíveis.
- Cada aluno deve baixar o relatório final HTML e entregá-lo ao professor. O relatório HTML é o único arquivo que o aluno precisa baixar e entregar, salvo orientação diferente do professor.
- Para que o professor receba e acompanhe as respostas automaticamente em um painel, será necessário adicionar um backend ou serviço de banco de dados.

## Limitações
- Não há login real, pagamentos reais, banco de dados central ou envio automático dos resultados.
- Não use dados pessoais além do nome/turma para identificar o trabalho, nem credenciais reais.
- Os defeitos são intencionais e simulados para aprendizagem.

## Manutenção e reinicialização segura
- Os botões para apagar todos os testes e apagar todos os defeitos foram removidos das telas de execução.
- Também foi removida a exclusão individual de defeitos e o botão de limpar o formulário de registro.
- A única opção de reinicialização fica em **Finalizar atividade > Manutenção da atividade**.
- Para confirmar, o aluno precisa abrir a confirmação e digitar exatamente `APAGAR TUDO`, em um fluxo de confirmação inspirado em ações destrutivas do GitHub.
- A reinicialização apaga a identificação atual, os resultados/observações e defeitos associados a essa identificação neste navegador. É irreversível; recomenda-se baixar o relatório antes.
- O botão **Esvaziar carrinho** foi mantido porque é uma ação funcional necessária para executar testes de carrinho vazio; ele não apaga os resultados ou defeitos registrados.


## Interface e avisos
- A interface usa espaçamentos consistentes entre cartões, campos e grupos de ações, com adaptação para telas pequenas.
- Pesquisa de produtos e área de login ficam em cartões separados; a lista de produtos e o carrinho também têm áreas próprias.
- Os avisos usam cores semânticas: azul para informação, amarelo para atenção, verde para conclusão e vermelho para erros ou ações destrutivas.
- A conferência final exige identificação, status para os 12 casos e observação para cada teste. O registro de defeitos é recomendado quando o aluno identifica uma falha, mas não bloqueia a finalização; isso evita confundir o relatório final com um checklist de defeitos obrigatórios.
