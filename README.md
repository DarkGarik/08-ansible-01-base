# Самоконтроль выполнения задания

1. Где расположен файл с `some_fact` из второго пункта задания?

    Файл [`examp.yml`](group_vars/all/examp.yml) находится по пути [group_vars/all](group_vars/all)

2. Какая команда нужна для запуска вашего `playbook` на окружении `test.yml`?

    Необходимо выполнить следующую команду: `ansible-playbook site.yml -i inventory/test.yml`

3. Какой командой можно зашифровать файл?

    `ansible-vault encrypt group_vars/deb/examp.yml`

4. Какой командой можно расшифровать файл?

    `ansible-vault decrypt group_vars/deb/examp.yml`

5. Можно ли посмотреть содержимое зашифрованного файла без команды расшифровки файла? Если можно, то как?

    Можно. Для этого можно воспользоваться командой `ansible-vault view  group_vars/deb/examp.yml`

6. Как выглядит команда запуска `playbook`, если переменные зашифрованы?

    `ansible-playbook site.yml -i inventory/prod.yml --ask-vault-pass`

7. Как называется модуль подключения к host на windows?

    Можно воспользоваться модулем `winrm` или через Microsoft PowerShell Remoting Protocol с помощью модуля `psrp`

8. Приведите полный текст команды для поиска информации в документации ansible для модуля подключений ssh

    `ansible-doc -t connection ssh`

9.  Какой параметр из модуля подключения `ssh` необходим для того, чтобы определить пользователя, под которым необходимо совершать подключение?

    ```
    - remote_user
        User name with which to login to the remote server, normally set by the remote_user keyword.
        If no user is supplied, Ansible will let the SSH client binary choose the user as it normally.
        [Default: (null)]
        set_via:
          cli:
          - name: user
            option: --user
          env:
          - name: ANSIBLE_REMOTE_USER
          ini:
          - key: remote_user
            section: defaults
          vars:
          - name: ansible_user
          - name: ansible_ssh_user
        
    ```
