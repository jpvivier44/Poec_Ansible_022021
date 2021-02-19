# TP Utilisation role galaxy 

## Déploiement d'un docker host

1) Récupérer le rôle docker suivant :

    https://github.com/geerlingguy/ansible-role-docker

    > Par ansible-galaxy !!
     
    > Utiliser le fichier requirements.yaml

2) Créer un groupe docker dans l'inventaire
    - Y associer la machine cliente de type debian

3) Créer un playbook install-docker-playbook.yaml
    - Target : docker
    - utilise le role docker pour installer docker sur la vm debian

4°) Récuperer le rôle suivant :

    https://github.com/geerlingguy/ansible-role-pip

5°) Utiliser le role pip, dans un nouveau playbook : deploy-docker-app-playbook.yaml

    - specifier une variable pour installer la librairie docker

6°) Utilisation du module  community.docker.docker_image pour faire un pull d'une image docker
    - Necessite l'installation de la collection : community.docker
    ```ansible-galaxy collection install community.docker```

7°) Realisation d'un structure de données de variables pour deployer plusieurs images et plusieurs conteneurs via des loop