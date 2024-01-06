1.  Firstable, you should switch to the correct branch into ola-api repository
```
git switch SECURE-LOAN
```

2. Second, you have to open a new terminal but, with _git bash terminal._

4. Then, type this command and press enter key.
```
eval "$(ssh-agent -s)"
```

4. Now, you have to type this command and press enter.
```
ssh-add ~/.ssh/id_rsa3
```

> [!NOTE]
> (You are going to enter your password for your ssh key)

>[!IMPORTANT]
> Note: It is really important to change _</.ssh/id_rsa3>_ for your right ssh public key path

5. Now, you have to pull all the changes from SECURE-LOAN branch of Azure Repositories.
```
git pull techywe SECURE-LOAN
```

6. Once you have all the changes from the branch SECURE-LOAN, it is time to _merge_ into the ola-api repository from bbl github.
```
git merge SECURE-LOAN tp1-bbldev
```

> [!WARNING]
> If there are conflicts while mixing the branches, they should be resolved in the first instance.

7. Then, just push all the necessary commits to the ola-api repository.
```
git push origin tp1-bbldev
```
