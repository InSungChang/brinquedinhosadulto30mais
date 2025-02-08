# brinquedinhosadulto30mais
Site afiliado brinquedinhosadulto30mais

Video para criação de vários ambientes de aprovações, nesse exemplo foram criados, desenvolvimento, staging (ambiente de testes) e produção.
https://youtu.be/lfoYZ1tz33k?si=Gn2Uk8yAbt3c9ow0

Ajustes para corrigir o problema de Github Actions

### **🔧 Correções realizadas no `deploy.yml`**
1️⃣ **Correção da configuração da chave SSH**  
   - Antes: O caminho da chave SSH estava incorreto (`~/.ssh/deploy_key_u907364100_1738968201884`).  
   - Agora: A chave SSH é criada corretamente no ambiente (`~/.ssh/id_ed25519`).  

2️⃣ **Correção de permissões na chave SSH**  
   - Antes: A chave SSH não tinha permissão correta, causando erro de acesso.  
   - Agora: O comando `chmod 600 ~/.ssh/id_ed25519` foi adicionado para garantir segurança e funcionamento.  

3️⃣ **Correção do `known_hosts` para evitar aviso de segurança**  
   - Antes: O SSH pedia confirmação manual ao conectar no servidor.  
   - Agora: O `ssh-keyscan` adiciona automaticamente a chave do servidor ao `known_hosts`.  

4️⃣ **Correção da estrutura do `deploy.yml`**  
   - Antes: A tentativa de conexão SSH ocorria antes da configuração da chave.  
   - Agora: A chave SSH é configurada antes de testar a conexão.  

---

Agora seu **GitHub Actions está funcionando corretamente** para conectar ao servidor Hostinger sem pedir senha! 🎉  

Se quiser guardar essas anotações de forma mais organizada, pode criar um **arquivo `README.md`** no repositório e registrar as mudanças.  

Me avise se precisar de mais alguma coisa! 🚀💪