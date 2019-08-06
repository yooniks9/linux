## ansible-playbook cli

#### prompt for password
```
ansible-playbook playbook.yml --user=username --ask-sudo-pass
```

#### include password on cli
```
ansible-playbook playbook.yml --user=username --extra-vars "ansible_sudo_pass=yourPassword"
```
