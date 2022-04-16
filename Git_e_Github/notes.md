# Como o Git realmente funciona?

- SHA1: Secure Hash Algorithm projetado pela NSA, toda vez que um arquivo é alterado, uma nova string de 40 dígitos é gerada.

- Objetos fundamentais:
  
  - Blobs - É um objeto contendo metadados e o conteúdo dos arquivos no git, não vai guardar o nome dos arquivos, apenas os seus SHA1
  - Trees - Armazenam e blobs e apontam para os mesmos quando necessário. Também guarda metadados e guarda o nome do arquivo e as árvores também tem um SHA1 dos metadados das árvores
  - Commit - Aponta para um árvore, para um parente, um autor ou uma mensagem.

- Sistema distribuído

- Segurança

- Os arquivos da máquina, para o git podem ser tracked ou untracked, sendo que no primeiro ainda tem 3 subdivisões:
  
  - Unmodified: Um arquivo que já existia antes da criação do repositório, mas ainda não foi modificado
  
  - Modified: Um arquivo que estava presente na criação do repositório e foi modificado
  
  - Staged: É quando o arquivo está se “preparando” para fazer parte de um commit. Quando o commit o feito, os arquivos retornam para unmodified.
    
    Quando rodamos um git add, movemos um arquivo untracked direto para o staged.
    
    Quando um arquivo que já existia com o início do repositório é modificado, ele passa de unmodified para modified, para colocá-lo no staged, basta rodar um git add
    
    Deixar os arquivos em staged permite que você trabalhe em outros arquivos sem necessariamente fazer um update de todas as alterações.
    
    É importante sempre fazer commits de pequenas alterações que se relacionem entre si.
    
    ![lifecycle.png](/home/davileal/Documentos/Coding/Carrefour-WebDeveloper/notes/Assets/lifecycle.png)
    
    Ao usar o git, você divide o projeto entre o repositório remoto e as máquinas locais.
    
    As máquinas locais serão dividas logicamente em:
  
  - Working Directory: O seu diretório local, a sua máquina
  
  - Staging Area: Um lugal para onde os arquivos do working directory, serão “separados” para transformá-los em um commit.
  
  - Local Repository: Os arquivos virão até o repositório local através de commits, antes de no fim ser enviados para o repositório remoto.