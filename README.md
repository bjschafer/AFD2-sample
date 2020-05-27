# AFD2 sample control repo

## Initial setup

### Pre-commit hook / vault validation
Please symlink the pre-commit hook into your git directory with `ln -s pre-commit.sh .git/hooks/pre-commit`.

This will help you by ensuring ansible-vault files are encrypted, and that you don't put incorrect variables in.

### Vault setup

For local use at least, create a file called `vault.pass`. Its only contents should be the vault password. That file is in `.gitignore` so you shouldn't accidentally commit it. Then, it won't prompt for a password when running the playbook.

Any files that are encrypted with vault should have the extension `.vault.yaml`, instead of `.yaml`.
