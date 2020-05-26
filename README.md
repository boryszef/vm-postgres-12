# Prepare vagrant box with Postgresql-12

Install ansible:
```shell
python3 -m venv venv
source venv/bin/activate
pip install ansible
```

Start VM:
```shell
vagrant up
```

Provision the VM:
```shell
ssh-keygen -t rsa -f ssh_key
echo YOUR_PASSWORD > postgres.pass
ansible-playbook playbook.ini
```

Log into the VM:
```shell
vagrant ssh
```
