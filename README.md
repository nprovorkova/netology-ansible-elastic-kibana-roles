### 8.4 Работа с Roles - Наталия Проворкова
###### 1. Создать в старой версии playbook файл requirements.yml и заполнить его следующим содержимым:
"---
  - src: git@github.com:netology-code/mnt-homeworks-ansible.git
    scm: git
    version: "2.0.0"
    name: elastic "
#### 2. При помощи ansible-galaxy скачать себе эту роль.
![roles_2](imgs/roles_2.png)
#### 3. Создать новый каталог с ролью при помощи ansible-galaxy role init kibana-role.
![roles_3](imgs/roles_3.png)
###### 4. На основе tasks из старого playbook заполните новую role. Разнесите переменные между vars и default.
###### 5. Перенести нужные шаблоны конфигов в templates.
#### 6. Создать новый каталог с ролью при помощи ansible-galaxy role init filebeat-role.
![roles_6](imgs/roles_6.png)
###### 7. На основе tasks из старого playbook заполните новую role. Разнесите переменные между vars и default.
###### 8. Перенести нужные шаблоны конфигов в templates.
###### 9. Описать в README.md обе роли и их параметры.
#### 10. Выложите все roles в репозитории. Проставьте тэги, используя семантическую нумерацию.
###### 11. Добавьте roles в requirements.yml в playbook.
#### 12. Переработайте playbook на использование roles.
 ansible-galaxy install -r requirements.yml<br>
![12_1](imgs/12_1.png)<br>
 ansible-galaxy install -r requirements.yml --force<br>
![12_2](imgs/12_2.png)<br>
ansible-playbook -i inventory/prod site.yml<br>
![12_2](imgs/12_3.png)<br>
![12_2](imgs/12_4.png)<br>
![12_2](imgs/12_5.png)<br>
Elasticsearch работает<br>
![12_elastic](imgs/12_elastic.png)<br>
Kibana работает<br>
![12_kibana](imgs/12_kibana.png)<br>
Filebeat не подключается к Kibana, не понятно почему<br>