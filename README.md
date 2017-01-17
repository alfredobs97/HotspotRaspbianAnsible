<h1>Hotspot de manera automática en Raspberry pi3 usando Ansible</h1>
**Instalación de Ansible**

 *Ubuntu-APT:*
```
 $ sudo apt-get install software-properties-common
 $ sudo apt-add-repository ppa:ansible/ansible
 $ sudo apt-get update
 $ sudo apt-get install ansible
 ```
 *Debian-APT:*
 ```
  $ sudo apt-get update
  $ sudo apt-get install python-pip python-dev git -y
  $ sudo pip install PyYAML jinja2 paramiko
  $ git clone https://github.com/ansible/ansible.git
  $ cd ansible
  $ sudo make install
  $ sudo mkdir /etc/ansible
  $ sudo cp ~/ansible/examples/hosts /etc/ansible/
  ```
1. Configuramos la ip de la raspeberry en la que vamos a crear el hotspot en el archivo */etc/ansible/host/*
2. cd HotsportRaspbianAnsible
3. ansible-playbook install.yml
4. El SSID: *YourSSIDName* y password:*ansiblerules* Estos parametros se pueden configurar en el archivo *templates/hostapd.conf.j2*
