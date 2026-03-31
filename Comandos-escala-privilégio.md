# 31/03/26
# Estudando comandos básicos para escala de privilégios no meu LAB de testes.

- hostname: mostra o nome do dispositivo(seu pc) na rede.
  
   - ubuntu(nome do pc na rede)

- whoami: mostra o nível de permissão do usuário

  - joao (pemissão padrão esse user)
    - root (permissão total do sistema)


- id(identifiction): identifica informações básicas do usuário:

  - uid=1001(joao) gid=1001(joao) groups=1001(joao),100(users)
      
    - uid(user ID): endereço do usuário
    - gug(group ID): grupo principal que o user faz parte.
    - groups: outros grupos que o user faz parte(sem ser o principal).
      
- ls -la: lista tudo em um diretório(mostra data,permisões e tamanho do conteúdo)

  - rwx-rwx-rwx:
    - 1° campo = permissões do dono do conteúdo
    - 2° campo = permissões do grupo do dono
    - 3° campo = permissões pra quem é de fera do grupo do dono    
    - 4(situacional): " - " sem permissão.
      
  - diretórios e arquivos:

     - diretório: "d"
     - arquivo padrão: "-"
     - arquivos especiais: "." vem antes do nome do arquivo.
     - 
- permissões         

   - r (read/leitura): permite acessar um arquivo, mas não escrever e modificar.
   - w (write/escrita): permite acessar e escrever no arquivo
   - x (execution/execução): permite executar algum arquivo(script).

   



   
   
