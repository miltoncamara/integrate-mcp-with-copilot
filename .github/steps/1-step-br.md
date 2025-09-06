# Etapa 1: Introdução ao MCP e configuração do ambiente

<img width="150" align="right" alt="copilot logo" src="https://github.com/user-attachments/assets/4d22496d-850b-4785-aafe-11cba03cd5f2" />

No exercício [Getting Started with GitHub Copilot](https://github.com/skills/getting-started-with-github-copilot), fomos apresentados ao site de atividades extracurriculares da Escola Mergington High School, que permitia que os alunos se inscrevessem em eventos.

E agora temos um problema... mas um bom problema! Mais professores estão pedindo para usá-lo! 🎉

Nossos colegas professores têm muitas ideias, mas não conseguimos acompanhar todos os pedidos! 😮 Para resolver isso, vamos dar um upgrade no GitHub Copilot habilitando o **Model Context Protocol (MCP)**. Mais especificamente, vamos adicionar o **servidor MCP do GitHub**, que permitirá um fluxo combinado de **gestão de issues** e **atualizações no site**. 🧑‍🚀

Vamos começar!

---

## O que é o Model Context Protocol (MCP)?

O [Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) é frequentemente chamado de **"USB-C para IA"** – um conector universal que permite ao GitHub Copilot (e outras ferramentas de IA) interagir facilmente com outros serviços.

Basicamente, é uma forma de descrever as capacidades e requisitos de um serviço, de forma que ferramentas de IA possam identificar quais métodos usar e quais parâmetros fornecer corretamente. Um servidor MCP fornece essa interface.

```mermaid
graph LR
    A[Desenvolvedor] -->|Usa| B[GitHub Copilot]
    B -->|API Unificada| MCP[Model Context Protocol]

    MCP <-->|API Única| C[(GitHub)]
    MCP <-->|API Única| D[(Slack)]
    MCP <-->|API Única| E[(Figma)]

    style B fill:#4CAF50,stroke:#333,stroke-width:2px

    subgraph "Menos Troca de Contexto, Mais Código"
        B
        MCP
        C
        D
        E
    end
```

---

## :keyboard: Atividade: Conhecendo o ambiente

Antes de mergulhar no MCP, vamos iniciar nosso ambiente de desenvolvimento e relembrar o aplicativo de atividades extracurriculares.

1. Clique com o botão direito no botão abaixo para abrir a página **Create Codespace** em uma nova aba. Use a configuração padrão.

   [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

2. Valide se as extensões **Copilot Chat** e **Python** estão instaladas e habilitadas.

   <img width="300" alt="copilot extension for VS Code" src="https://github.com/user-attachments/assets/ef1ef984-17fc-4b20-a9a6-65a866def468" /><br/>
   <img width="300" alt="python extension for VS Code" src="https://github.com/user-attachments/assets/3040c0f5-1658-47e2-a439-20504a384f77" />

3. Verifique se o aplicativo roda antes de modificá-lo. Na barra lateral esquerda, selecione a aba **Run and Debug** e pressione o ícone **Start Debugging**.

   <details>
   <summary>📸 Mostrar captura de tela</summary><br/>

   <img width="300" alt="run and debug" src="https://github.com/user-attachments/assets/50b27f2a-5eab-4827-9343-ab5bce62357e" />

   </details>

   <details>
   <summary>🤷 Com problemas?</summary><br/>

   Se a área de **Run and Debug** estiver vazia, tente recarregar o VS Code: Abra a paleta de comandos (`Ctrl`+`Shift`+`P`) e procure por `Developer: Reload Window`.

   <img width="300" alt="empty run and debug panel" src="https://github.com/user-attachments/assets/0dbf1407-3a97-401a-a630-f462697082d6" />

   </details>

4. Use a aba **Ports** para encontrar o endereço da página web, abra-o e verifique se está rodando.

   <details>
   <summary>📸 Mostrar captura de tela</summary><br/>

   <img width="350" alt="ports tab" src="https://github.com/user-attachments/assets/8d24d6b5-202d-4109-8174-2f0d1e4d8d44" />

   ![Screenshot of Mergington High School WebApp](https://github.com/user-attachments/assets/5cb88d53-d948-457e-9f4b-403d697fa93a)

   </details>

---

## :keyboard: Atividade: Adicionar o servidor MCP do GitHub

1. Dentro do seu codespace, abra o painel **Copilot Chat** e verifique se o modo **Agent** está selecionado.

   <img width="200" alt="image" src="https://github.com/user-attachments/assets/201e08ab-14a0-48bf-824e-ba4f8f43f8ab" />

   <details>
   <summary>Modo Agent ausente?</summary><br/>

   - Verifique se o VS Code está na versão `v1.99.0` ou superior.
   - Verifique se a extensão do Copilot está na versão `v1.296.0` ou superior.
   - Confira se o modo Agent está habilitado nas [configurações de usuário ou workspace](https://code.visualstudio.com/docs/configure/settings#_workspace-settings).

      <img width="300" alt="image" src="https://github.com/user-attachments/assets/407a79dd-707e-471b-b56b-1938aece4ad8" />

   </details>

2. No seu codespace, navegue até a pasta `.vscode` e crie um arquivo chamado `mcp.json`. Cole o seguinte conteúdo:

   📄 **.vscode/mcp.json**

   ```json
   {
     "servers": {
       "github": {
         "type": "http",
         "url": "https://api.githubcopilot.com/mcp/"
       }
     }
   }
   ```

3. No arquivo `.vscode/mcp.json`, clique no botão **Start** e aceite o prompt para autenticar com o GitHub. Isso informou ao GitHub Copilot as capacidades do servidor MCP.

   <img width="350" alt="mcp.json file showing start button" src="https://github.com/user-attachments/assets/15a3d885-1c13-40b4-8d59-87b478ddd8a0" />

   <img width="350" alt="allow authentication prompt" src="https://github.com/user-attachments/assets/f5ec128d-9924-454b-8ab4-3f43ebc83cfc" /><br/>

   <img width="350" alt="mcp.json file showing running server" src="https://github.com/user-attachments/assets/c413c52d-94dc-429f-91e0-3486141908b9" />

4. No painel lateral do Copilot, clique no ícone **🛠️** para mostrar as capacidades adicionais.

   <img width="350" alt="image" src="https://github.com/user-attachments/assets/b1be8b80-c69c-4da5-9aea-4bbaa1c6de10" />

   <img width="350" alt="image" src="https://github.com/user-attachments/assets/99178d1b-adbe-4cf4-ab9c-3a4d29918a13" />

5. **Commit** e **push** o arquivo `.vscode/mcp.json` para a branch `main`.

   > 🪧 **Nota:** Fazer push direto para a branch `main` não é uma boa prática. Estamos fazendo isso apenas para simplificar este exercício.

6. Agora que sua configuração do servidor MCP foi enviada para o GitHub, a Mona já deve estar verificando seu trabalho. Aguarde um pouco e fique de olho nos comentários. Você verá ela respondendo com informações de progresso e a próxima lição.

> [!NOTE]
> Os próximos passos envolverão a criação de issues no GitHub. Se quiser evitar receber notificações por e-mail, você pode parar de seguir o repositório.

<details>
<summary>Com problemas?</summary><br/>

Certifique-se de que:

- Seu arquivo `.vscode/mcp.json` é semelhante ao exemplo fornecido.
- Você fez push das alterações para a branch `main`.

</details>
