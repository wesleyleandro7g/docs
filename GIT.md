# GIT

## Remover uma pasta do repositório

Primeiro certifique-se que o seu repositório está sincronizado com o repositório remoto (supondo que o branch seja master):

    git pull origin master

Então remova a pasta localmente:

    git rm -r node_modules.

Agora faça um commit das modificações:

    git commit -m "Remove pastas Node_Modules"

Sincronize com repositório remoto:

    git push origin master

---

## Para dar um push em uma nova branch

- git add .
- git commit -m 'Commit'
- crie a nova branch
- git push --set-upstream origin nome-da-branch
