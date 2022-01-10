# Born2beroot
disk password -> 246813579Born2beroot
root - Ivinvlad1998
oarnoldo - Userlogin1

--------------------------------------------------------------
lsblk - посмотреть разбивку дисков
sudo - что то вроде админских прав
sudo adduser [name] [group] - добавить пользователя в группу
sudo addgroup [groupname] - добавить группу пользователей
getent group [groupname] - посмотреть кто входит в группу

apt - установщик программ
sudo aa-status
nano /etc/sudoers.d/ - sudo config
nano /etc/login.defs - установка срока паролей
nano /etc/pam.d/common-password - ограничения паролей
sudo crontab -l
sudo nano /etc/hostname - смена имени ос
sudo servise cron [stop/start/status]
sudo chage -l [username] - заставить пользователя сменить пароль
--------------------------------------------------------------
openssh-server - (/etc/ssh/ssh_config, /etc/ssh/sshd_config) позволяет настроить удаленное подключение
ufw - брандмауэр дает доступ приложениям в сеть а так же ограничивает или разрешает доступ к системе по портам (ufw allow [port], ufw status)
ssh <oarnoldo>@localhost -p 4242
sudo service ssh status
sudo ufw status
sudo ufw [deny/allow] [port]
----------------------------------------------------------------
sudo log
sudo mkdir /var/log/sudo
sudo touch /etc/sudoers.d/sudoconfig
sudoconfig ->
Defaults passwd_tries=3
Defaults badpass_message="Incorrect password"
Defaults log_input,log_output
Defaults iolog_dir="/var/log/sudo"
Defaults requiretty
Defaults secure_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"
----------------------------------------------------------------
настройки паролей
sudo nano /etc/login.defs - позволяет настроить min/max срок действия паролей
apt libpwquality - проверяет качество паролей и позволяет их генерировать
https://itsecforu.ru/2019/02/18/%D0%BA%D0%B0%D0%BA-%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D0%BD%D0%B8%D1%82%D1%8C-%D0%BF%D0%BE%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D1%83-%D0%BD%D0%B0%D0%B4%D0%B5%D0%B6%D0%BD%D1%8B%D1%85-%D0%BF%D0%B0%D1%80%D0%BE/
сменить пароль - passwd
nano /etc/pam.d/common-password
----------------------------------------------------------------
