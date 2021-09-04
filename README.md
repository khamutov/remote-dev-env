# Setup remote dev server

## 1. Add host to ssh config and enable ssh key forwarding

```bash
Host <server_name>
   HostName <server_addr>
   User <user>
   ForwardAgent yes
```

## 2. Check ssh-agent keys

```
ssh-add -l
```

add ssh-key if not present

```
ssh-add ~/.ssh/<your_key>
```

## 3. Add target host to `inventories/inventory`

```
[dev_hosts]
test_srv
```

## 4. Run dev env provision

```bash
ansible-playbook playbook.yml
```
