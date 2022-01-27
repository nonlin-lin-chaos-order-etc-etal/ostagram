# Ostagram
Данное web-приложение является web надстройкой над программой по обработке изображения нейронными сетями. Для создания картин используется сверточные
нейронные сети и алгоритм художественно стиля by Leon A. Gatys, Alexander S. Ecker, and Matthias Bethge. Более подробно с этим можно ознакомиться по ссылке на GitHub ниже.

This program is a web service for algorithm combining the content of one image with the style of another image using convolutional neural networks.

## Running this project

### Gitpod

To deploy this project to Gitpod, click this link:

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#github.com/nonlin-lin-chaos-order-etc-etal/ostagram)



## Requirements

Test with Rails 4.2


## Installation

Для работы web-приложения необходимо создать config.secret в папке config примерно со следующим содержанием:

```yaml
token:
  production: - ключ сессии

workservers:
  server1:
    host: "deploy" - адрес удаленного сервера для обработки
    username: "deploy" - логин
    password: "пароль"
    remote_neural_path: "/home/deploy/neural-style" - путь где распологается сеть
    init_params: "-gpu -1 -image_size 100" - строка инициализации для сети
    iteration_count: 10 - количество итераций обработки
    admin_email: "почта_админа@gmail.com"

smtp_settings:
  address: 'smtp.gmail.com'
  port: 587
  domain: 'gmail.com'
  user_name: 'почта_отправки_результата@gmail.com'
  password: 'пароль'
  authentication: 'plain'
  enable_starttls_auto: true
```

## More Information

The neural network used is https://github.com/jcjohnson/neural-style
