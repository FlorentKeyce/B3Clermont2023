Projet Ansible de déploiement d'une infrastructure web (http/php/mariadb).

Nécessite un rôle Ansible Galaxy :
                ansible-galaxy install --roles-path ./roles/ -r requirements.yml

Comment l'utiliser :

- Etape 1 : Inventaire
                Copier et compléter "inventory.example" en "inventory"

- Etape 2 (facultative) : mise à jour d'Ansible
                ansible-playbook playbook-controlnode.yml 

- Etape 3 (à faire une seule fois) : déployer la clé publique SSH de Ansible 
                export ANSIBLE_HOST_KEY_CHECKING=False
                ansible-playbook --ask-pass playbook-ssh.yml

- Etape 4 : déploiement "principal" :
                ansible-playbook playbook-all.yml