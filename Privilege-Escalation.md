-  O que é Privilege Escalation?

- Privilege escalation (escalonamento de privilégios) é quando um usuário ou processo 
  ganha mais permissões do que deveria ter dentro de um sistema.

- Exemplo simples:

   - Você entra como usuário comum
   - Explora uma falha
   - Vira administrador/root


- Tipos principais

   - 1. Escalada Vertical
      Aumenta o nível de privilégio

      - Ex: usuário comum → admin/root


   - 2. Escalada Horizontal
      Acessa recursos de outro usuário no mesmo nível
      - Ex: invadir conta de outro usuário sem virar admin


- Como isso acontece na prática?

- Alguns vetores comuns:

-  Em sistemas (Linux/Windows):

   - Permissões mal configuradas
   - Binários com SUID (Linux)
   - Serviços vulneráveis
   - Tarefas agendadas mal protegidas


-  Em aplicações web:

   - Falhas de autorização (Broken Access Control)
   - Manipulação de tokens/cookies
   - APIs sem validação correta


-  Exemplos clássicos no Linux:

   - Arquivos com SUID
   - Uso indevido de sudo
   - PATH hijacking


- Windows:

   - Serviços rodando como SYSTEM
   - DLL hijacking
   - Weak registry permissions


-  Fluxo básico de exploração:
   - Acesso inicial:

      - (ex: shell básica ou login)
      - Enumeração  (etapa mais importante!)
      - Usuário atual
      - Permissões
      - Processos rodando
      - Arquivos interessantes
      - Identificação de vulnerabilidades
      - SUID
      - Configs erradas
      - Credenciais expostas
      - Exploração
      - Usar falha para subir privilégio


- Pós-exploração:
   - Manter acesso
   - Coletar dados (em ambiente controlado)


- Conceitos importantes pra estudar junto: 
   - Princípio do menor privilégio
   - Controle de acesso (RBAC/ABAC)
   - Hardening de sistemas
   - OWASP Top 10 (especialmente Broken Access Control)





