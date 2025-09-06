# Modo Admin  
   
## Problema  
   
Os alunos estão removendo uns aos outros para liberar espaço para si mesmos nas atividades.  
   
## Solução Recomendada  
   
Adicionar um ícone de usuário no canto superior direito. Ao clicar, mostra um botão de login. Quando o botão de login for clicado, apresenta uma janela para inserir nome de usuário e senha.  
   
- Apenas os professores (logados) terão a capacidade de registrar e desregistrar alunos nas atividades.  
   
- Os alunos (não logados) ainda poderão visualizar quem está registrado.  
   
- Não há necessidade de uma página de manutenção de conta. Os professores terão senhas atribuídas.  
   
## Contexto  
   
Como ainda não há banco de dados, por favor, armazene os nomes de usuário e senhas dos professores em um arquivo `json` que será verificado pelo backend.