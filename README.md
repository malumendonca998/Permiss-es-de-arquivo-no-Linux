# Projeto de Auditoria de Permissões no Sistema de Arquivos 📂🔍  

Este projeto foi desenvolvido para realizar uma auditoria nas permissões de arquivos e diretórios em um sistema de arquivos, garantindo que as permissões estejam alinhadas com as necessidades de cada usuário ou grupo de usuários. O foco principal foi assegurar que os membros da equipe de pesquisa tenham acesso apenas aos arquivos e diretórios necessários para suas atividades, seguindo o princípio do menor privilégio. 🚀  

---

## Objetivo 🎯  
- Verificar e ajustar as permissões de arquivos e diretórios para garantir conformidade com as políticas de segurança.  
- Aplicar o princípio do menor privilégio, garantindo que usuários e grupos tenham apenas as permissões necessárias para suas funções.  

---

## Tecnologias Utilizadas 💻  
- **Sistema Operacional:** Linux 🐧  
- **Comandos:** Utilização de comandos do terminal Linux, como `ls`, `chmod`, e scripts em **Bash** para automatizar a verificação e alteração de permissões.  

---

## Metodologia 📝  

### 1. Verificação das Permissões Atuais  
Foram utilizados os seguintes comandos do Linux para listar e analisar as permissões dos arquivos e diretórios:  
- `ls`: Lista os arquivos e diretórios.  
- `ls -l`: Exibe as permissões detalhadas.  
- `ls -a`: Lista arquivos ocultos.  
- `ls -la`: Combina as permissões detalhadas com a exibição de arquivos ocultos.  

### 2. Descrição das Permissões Atuais  
Foram analisados os seguintes arquivos:  
- **project_k.txt:**  
  - 👤 Usuário: Leitura (r) e Escrita (w)  
  - 👥 Grupo: Leitura (r) e Escrita (w)  
  - 🌍 Outros: Leitura (r) e Escrita (w)  
- **project_m.txt:**  
  - 👤 Usuário: Leitura (r) e Escrita (w)  
  - 👥 Grupo: Leitura (r)  
  - 🌍 Outros: Nenhuma permissão  
- **project_r.txt:**  
  - 👤 Usuário: Leitura (r) e Escrita (w)  
  - 👥 Grupo: Leitura (r) e Escrita (w)  
  - 🌍 Outros: Leitura (r)  
- **project_t.txt:**  
  - 👤 Usuário: Leitura (r) e Escrita (w)  
  - 👥 Grupo: Leitura (r) e Escrita (w)  
  - 🌍 Outros: Leitura (r)  

### 3. Alteração de Permissões  
Foram realizadas as seguintes alterações utilizando o comando `chmod` no terminal Linux:  
- **project_k.txt:**  
  - Remoção da permissão de escrita (w) para "outros":  
    ```bash  
    chmod o-w project_k.txt  
    ```  
- **.project_x.txt (arquivo oculto):**  
  - Remoção da permissão de escrita (w) para usuário e grupo, e adição da permissão de leitura (r) para o grupo:  
    ```bash  
    chmod u-w,g-w,g+r .project_x.txt  
    ```  

---

## Resultados 📊  
- As permissões foram ajustadas para garantir que os usuários e grupos tenham apenas as permissões necessárias. ✅  
- O princípio do menor privilégio foi aplicado, aumentando a segurança do sistema e reduzindo o risco de acesso não autorizado a arquivos sensíveis. 🔐  

---

## Como Executar o Projeto 🚀  
1. Clone o repositório:  
   ```bash  
   git clone https://github.com/seu-usuario/auditoria-permissoes.git  
