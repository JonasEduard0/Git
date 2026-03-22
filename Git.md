# 📘 Git

## 📌 Conceitos

**Workspace:** O computador do programador, a área de trabalho.

**Staging Area (index):** Área intermediária onde seleciona quais mudanças do projeto irão para o próximo commit.

**Repositório Local (HEAD):** Versões oficiais ficam armazenadas localmente aqui.

**Repositório Remoto:** Onde ficam as versões na nuvem (GitHub, GitLab, etc).

**Commit:** Versão salva do código.

---

## ⚙️ Configuração inicial

`git --version` —                                 Versão atual do Git na máquina.  
`git config --global user.name "Seu Nome"` —      Configura, globalmente, um nome de usuário. Assim, todos sabem quem alterou.  
`git config --global user.email "a@gmail.com"` —  Cadastra um e-mail.  
`git config --global --list` —                    Mostra suas informações globais - nome e email.

---

## 🚀 Comandos

`git clone link-repositorio` — clona o repositório no PC e permite alterações.  
`cd pasta-repositorio` — entra na pasta do repositório.

`git init` — Inicializa/transforma uma pasta comum em um projeto versionado pelo Git.

`git add a.html` — coloca o arquivo do Workspace na Staging Area.  
`git add .` — adiciona todos os arquivos não adicionados à Staging Area.  

`git commit -m "txt"` — salva oficialmente no repositório local com uma mensagem.
`git diff` — mostra as diferenças entre versões de arquivos.

`git push` — envia para a nuvem.  
`git pull` — pega a versão atual do projeto no repositório remoto. 
`git fetch` — baixa as atualizações do repositório remoto sem aplicar no código.

`git checkout a1b2c3d` — volta para uma versão do código. `main`: volta ao presente (última versão).
`git checkout -b novo-design` - cria nova branch
`git switch nome-branch` — troca de branch ou cria e troca para uma nova branch(-c).
`git merge` - junta mudanças de uma branch em outra.

`git status` — mostra o estado atual do repositório.  
`git log` — histórico de commits. `--oneline`: resumido.

`git reset --soft HEAD~1` — desfaz o último commit (ainda sem `push`), mas os arquivos permanecem editados.  
`git reset --hard HEAD~1` — desfaz e descarta as mudanças.

---

## 🚫 Ignorar arquivos

Crie o arquivo `.gitignore` na raiz do projeto.  
Ignora os arquivos e pastas definidos nele. Nunca vai commitar esses arquivos.

---

## 📁 Após `git clone`

Dentro da pasta há o arquivo `README.md` e uma pasta oculta `.git`, que cuida das versões do sistema.  
Essa pasta está vinculada ao repositório remoto.

---

## ⚠️ Problema comum

Esquece de dar `git pull` antes de trabalhar.  
Trabalhou em uma versão antiga e, quando tenta `git push`, dá erro.

Tem que dar `git pull`. O Git mescla (`merge`) as mudanças e:

- se não tiver conflito, ok  
- se tiver conflito (você e alguém mexeram na mesma linha), o Git marca no arquivo e você decide qual versão manter  

Depois, edita manualmente, salva e faz commit.

---

## ✅ Boas práticas

Começar no imperativo, ser específico, objetivo e direto.  

Exemplo:  
`git commit -m "Corrige validação de email no formulário"`

Se precisar descrição mais detalhada:  
`git commit -m "Titulo" -m "Descricao grande"`

Faça um commit por tarefa.  
Evitar fazer muita coisa e commitar tudo junto.
