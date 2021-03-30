tarea de ansible del grupo 1 del diplomado de devops

1.- crear la maquina con el vagrantfile:
    os> vagrant up    

2.-copiar la llave para el usuario vagrant: (clave vagrant)  
    os> ssh-copy-id vagrant@192.168.33.11

3.-ejecutar ansible:
    os> ansible-playbook -i inventario jenkins.yml
    