

```
$ docker-compose run web django-admin startproject mysite .
```

編輯mysite/settings.py文件，將以下內容替換為數據庫配置部分：
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'mydatabase',
        'USER': 'myuser',
        'PASSWORD': 'mypassword',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```
在命令提示符中運行以下命令構建和運行Docker容器：
```
$ docker-compose up -d --build
```
創建一個新的Django應用。在命令提示符中運行以下命令：
```
$ docker-compose exec web python manage.py startapp dvdrental
```

```
$ docker-compose exec web python manage.py migrate
```

```
$ docker-compose up 
```