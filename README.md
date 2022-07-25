This is an example readme for an example project, this should be edited/extended/deleted as appropriate for the specific project 

# Ansible Template 
This project completes X tasks 

## requirements 

### Anisble controller 
- A linux server as a controller 
- ansible 2.9 or later installed 

### User 
- sudo access on the ansible controller 

## How to Use

### install ansible galaxy roles 
```
ansible-galaxy install --force -r requirements.yaml 
```
### How to run 
```
ansible-playbook -i hosts-<dev-env> playbook.yaml 
```

### How to run with tags 

tags can be provided to run specific tasks as part of the playbook 
```
ansible-playbook -i hosts-<dev-env> playbook.yaml -t deploy 
```

### Example Tags 
`build` - builds the application 

`deploy` - deploys the application 

`test` - smoke tests the application 

### Additional Variables 
The following variables can be overwritten while running the playbook 

| Variable                  | Purpose                                                     | Default                  | 
|---------------------------|-------------------------------------------------------------|--------------------------|
| Variable_1                | A flag to be set to true for X task to be completed         | false                    |
| Variable_2                | name to be used as a working directory                      | working-dir              |
