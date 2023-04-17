# pre-commit
Pre-commit Hooks

## Recommended configuration

Have all checks run:

```yaml
repos:
   - repo: https://github.com/mto79/pre-commit
     rev: v1.0.0
     hooks:
       - id: ansible_role_find_empty_files
       - id: ansible_role_find_empty_directories
```

You can also select single checks, read futher for more details.

## Ansible roles empty files finder

This hook can find empty `defaults/main.yml`, `handlers/main.yml` and `vars/main.yml` files.

```yaml
repos:
  - repo: https://github.com/mto79/pre-commit.git
    rev: v1.0.0
    hooks:
      - id: ansible_role_find_empty_files
```

Extra parameter available:

- `-l <number>`: number of minimum lines to declare that a file is empty (by default: 2)


## Ansible roles empty directory finder

This hook can find empty directories.

```yaml
repos:
  - repo: https://github.com/mto79/pre-commit.git
    rev: v1.0.0
    hooks:
      - id: ansible_role_find_empty_directory
```

Extra parameter available:

- `-d <number>`: number of sub folder (maxdepth) to check (by default: 1)
