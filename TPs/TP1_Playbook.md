# TP PLaybook - inventaire

## Gestion de l'inventaire

- le serveur client de type debian doit faire parti d'un groupe de l'inventaire appelé web

## Creation d'un playbook

- Fichier yaml : tp1-web-playbook.yaml

- Nom de play
- Target : web

- Tasks1 : s'assurer que les packages ci-dessous soient present : (module ??)
     - git
     - vim
     - apache2

- Tasks2 : S'assurer que le service apache2 soit activé (enable) et démarré (module ??)

- Tasks3 : Copie un fichier "static" index.html (présent dans le projet ansible) vers /var/www/html/index.html (module ??)
