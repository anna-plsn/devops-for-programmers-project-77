# Инфраструктура как код
### Hexlet tests and linter status:
[![Actions Status](https://github.com/anna-plsn/devops-for-programmers-project-77/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/anna-plsn/devops-for-programmers-project-77/actions)


## Описание
Автоматизация создания инфраструктуры проекта через Terraform и Ansible

## Требования к целевой машине
    - Ansible 
    - Trerraform CLI
    - openssl

## Установка
1. Запустите команду, изменить пароль на свой в файле `.vaultpassword`. 
```
make vault db_pass=<DB password> \
	   dd_api_key=<Datadog API key> \
	   dd_app_key=<Datadog Application key> \
	   yc_token=<Yandex clound Auth0 token> \
	   yc_cloud_id=<Yandex cloud id> \
	   yc_folder_id=<Yandex account folder id>
```
2. Уставнока terraform.
```
make terraform
```
3. Добавление ресурсов
```
make resources
```
4. Создание сервера
```
make deploy-full
```

### Описание дополнительного функционала
* Удалить инфраструтуру
```
make destroy
```
* Создать приложение локально
```
make local
```
* Установка Datadog
```
make datadog
```
* Заливка Book API
```
make deploy-book-api
```
* Установка Docker
```
make docker
```