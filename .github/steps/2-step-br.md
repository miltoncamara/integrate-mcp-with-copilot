## Passo 2: Modo Agente e um Servidor MCP para o GitHub

Ótimo trabalho! Você acabou de conectar seu primeiro servidor MCP ao
GitHub Copilot! 🎉

🚨 Parece que os professores continuam enviando bugs e solicitações!
Tantas boas ideias! Provavelmente devemos analisá-las e começar a
pesquisar outros aprimoramentos.

Felizmente, com um servidor MCP para o GitHub, triagem e até mesmo
pesquisa para se antecipar deve ser bem rápido! 🕵️

### Como usamos as ferramentas de um servidor MCP?

Boa notícia! Da mesma forma que você normalmente interage com o Copilot:
usando linguagem natural. Só lembre das capacidades disponíveis e das
restrições de permissão do seu token.

Com o servidor MCP disponível, agora podemos pedir ao Copilot coisas
além do nosso código. Aqui estão algumas ideias para imaginar as
possibilidades:

Por exemplo:

-   Pesquisar issues considerando descrição, comentários e curtidas.
-   Abrir, atualizar ou fechar issues em outro repositório.
-   Comparar repositórios.
-   Aprender sobre outros autores com quem você está trabalhando.
-   Recuperar uma issue, fazer alterações em um branch e iniciar um pull
    request.

Legal, né?! Agora vamos fazer isso! 👩‍🚀

### :keyboard: Atividade: Encontrar e salvar ideias rapidamente

1.  Feche quaisquer arquivos abertos no seu codespace. Isso ajudará a
    reduzir o contexto desnecessário.

2.  Certifique-se de que o painel **Copilot Chat** está aberto e o modo
    **Agente** está selecionado. Verifique também se as ferramentas do
    servidor MCP ainda estão disponíveis.

3.  Peça ao Copilot para pesquisar no GitHub projetos semelhantes a
    este.

    > ``` prompt
    > Search for any other repositories for organizing extra curricular activities
    > ```

4.  Quando uma ferramenta MCP for necessária, o Copilot pedirá
    permissão. **Verifique a solicitação** e modifique se necessário,
    depois clique em **Continuar**.

5.  Peça ao Copilot para descrever um dos projetos. Explore até
    encontrar algo que você goste.

    > ``` prompt
    > Please look at the code for the 3rd option and give me a detailed description of the features.
    > ```

6.  Use o Copilot para comparar e gerar ideias de melhorias.

    > ``` prompt
    > Please compare these features to our project. Which would be new?
    > ```

7.  Muito bom! Vamos pedir ao Copilot para criar issues para salvar
    essas ideias.

    > ``` prompt
    > I like it. Let's create issues for these in my repository.
    > ```

8.  O Copilot pedirá permissão para criar issues no seu repositório.
    Clique em **Continuar** para cada nova issue. Lembre-se: **verifique
    a solicitação** antes de executar.

9.  Como terminamos a pesquisa, finalize esta sessão de chat para limpar
    o contexto. No topo do painel **Copilot Chat**, clique no ícone
    **Novo Chat** (sinal de +).

10. Com as novas issues criadas, a Mona já deve estar verificando seu
    trabalho. Dê um momento e fique de olho nos comentários. Você verá
    ela responder com informações de progresso e a próxima lição.

> \[!NOTE\]\
> O ecossistema do **Model Context Protocol (MCP)** está evoluindo
> rapidamente. Muitos servidores, incluindo o [Servidor MCP Oficial do
> GitHub](https://github.com/github/github-mcp-server), estão em
> desenvolvimento ativo e ainda não têm paridade total com suas APIs
> estáveis.
