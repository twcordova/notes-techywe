>[!Note]
>You need to have installed the Putty Tool.

1. First, you have to enter as a super user:
```
su - olausr
```

**Pasword for super user**
```
Techy-WEE-2023!@!
```

2. You need to go to the api path, in this case will be `secure` which is `tp1-bbldev`

Here you have a reference of the different paths to access and make changes.

| Enviroment | Path |
| ---- | ---- |
| SECURE | /opt/OLA-ENVS/ola-api-1 |
| UNSECURE | /opt/OLA-ENVS/ola-api-2 |
```
cd /opt/OLA-ENVS/ola-api-1
```

3. Just to make sure, you can execute the command below to view the current status of the enviroments.
```
pm2 status
```

4. In this step is really important becuase you will get all the changes from the **Github** repository.
```
git pull origin tp1-bbldev
```

> [!Important]
> You have to change `tp1-bbldev` for the one you have to bring the data.

>[!Note]
>You are going to enter your Github Credentials (username and github key)
1. Now, you have to run the command below in order to have the compiled files for reloading after and make effect the changes you pull.
```
npm run pretest
```

5. Importante, make this command to reload the api.
```
pm2 reload ola1
```

>[!Important]
>You have to replace `ola1` for the reference enviroment viewed into the status command.

5. You can exec the `pm2 status` command just to make sure that the enviroment was refreshed.
6. If you want, you can run the command below to show the logs for the enviroment you want.
```
pm2 log ola1
```

>[!Important]
>You have to replace `ola1` for the reference enviroment viewed into the status command.

