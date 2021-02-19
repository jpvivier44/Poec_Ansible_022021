# Applications des connaissance :

## Modules, Handlers, variables, conditionnals, loop

### Reprise du playbook bootstrap-playbook.yaml

- Déclarer des variables

- S'assurer que openssh server soit bien installé
  - Une task par type de distri : (conditionnals when + fact "os_family" )
    - module apt (openssh-server)
    - module yum (openssh-server)

- Modifier la configuration du serveur openssh (/etc/ssh/sshd_config): (module lineinfile) => loop pour 2 modif
    - Activer le LogLevel
    - Desactiver le X11Forwarding

    > ATTENTION en cas de mauvaise syntaxe : penser au paramètre validate et backup

- SI modification du fichier sshd_config => reload du service sshd


### Tester le playbook :

- ansible-lint
- ansible-playbook --syntax-check
- ansible-playbook --check --diff

### Declenchement reel du playbook :

- ansible-playbook