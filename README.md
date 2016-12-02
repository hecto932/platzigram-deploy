# platzigram-deploy

```sh
vagrant up: Iniciar la maquina virtual
vagran destroy: Eliminar la maquina virtual
vagrat reload: Reinicia la maquina virtual
vagrant ssh: acceso consola por ssh. Si se realizo correctamnte la configuracion de las llaves.
```

```sh
ssh -p 2222 root@127.0.0.1 -i ssh/deploy
```

En el archivo inventory.ini definimos los servidores a los cuales ansible-playbook va a ejecutar ansible_ssh_port=2222

Para ejecutar ansible luego de realizar la configuracion de roles y tasks

```sh
ansible-playbook -i inventory.ini platzigram.yml --key-file ssh/deploy
```