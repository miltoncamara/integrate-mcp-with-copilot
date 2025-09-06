## Etapa 3: Resolver problemas com o Modo Agente e o Servidor MCP do GitHub

Ótimo trabalho fazendo a pesquisa e encontrando uma oportunidade de colaboração.  
Não só descobrimos novas ideias para ajudar a organizar atividades extracurriculares, como também fizemos isso bem rápido.

Assim sobra tempo para focar no que importa: ensinar nossos alunos incríveis! 🌱

Falando nisso, os professores também estiveram ativos.  
Parece que eles enviaram alguns bugs e pedidos! Perfeito! 🚀

Agora, vamos usar as ferramentas do nosso servidor MCP e o Copilot para fazer um pouco de triagem e colocar a mão na massa.

---

### :keyboard: Atividade: Implementar facilmente uma issue importante

1. Certifique-se de que o **painel do Copilot Chat** está aberto e o modo **Agente** selecionado. Verifique também se as ferramentas do servidor MCP ainda estão disponíveis.

2. Pergunte ao Copilot sobre as *issues* abertas neste repositório.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > How many open issues are there on my repository?
   > ```

   > 🪧 **Nota:** Confira se a ferramenta **List Issues** foi chamada com os parâmetros corretos.

3. Peça ao Copilot para resumir as *issues* importantes.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > Oh no. That's too many for me! Please get the list of issues,
   > review the descriptions and comments, and pick the top 3 most important.
   > ```

   <details>
   <summary><b>💡 Dica:</b> Pré-autorize o uso das ferramentas</summary><br/>

   Se o Copilot usar uma ferramenta com frequência, você pode conceder permissão de forma proativa para toda a sessão da conversa.

   <img width="350" src="https://github.com/user-attachments/assets/d741191e-4d98-489d-92d2-f1069fd6c34e"/>
   </details>

4. Revise as *issues* sugeridas.  
   Se o Copilot não recomendar algo específico, forneça feedback para refinar os resultados.

5. Com a lista reduzida, peça ao Copilot para implementar uma *issue*.  
   **A Mona não vai avaliar se as mudanças funcionam, apenas se uma tentativa foi feita.**

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > #codebase Vamos fazer a primeira. Siga estes passos:
   > 1. Crie uma nova branch local para as mudanças.
   > 2. Faça as alterações e depois confirme comigo se estão corretas.
   > 3. Envie as mudanças e abra um pull request.
   > ```

   > ⚠️ **Atenção:** Sempre verifique as ações que o Copilot está pedindo para executar, especialmente com as habilidades externas fornecidas por um servidor MCP, que provavelmente não possuem opção de desfazer.

6. Assim que o *pull request* for criado, a Mona começará a verificar seu trabalho.  
   Aguarde um momento e acompanhe os comentários. Você verá ela responder com informações de progresso e os próximos passos!

---

<details>
<summary>⚠️ Está com problemas?</summary><br/>

- Se as ferramentas não estiverem sendo chamadas, verifique se a configuração do MCP está correta.  
- Se o Copilot não conseguir obter resultados, confirme se você está usando o token deste Codespace ou um **Personal Access Token (PAT)** com permissões apropriadas.  
  Por padrão, o token do Codespace que estamos usando só tem acesso a este repositório.
</details>
