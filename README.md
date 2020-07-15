# ToDo application 📝
![GitHub last commit](https://img.shields.io/github/last-commit/PavelAndreyev1337/django-todo-react?style=flat-square) 
![GitHub](https://img.shields.io/github/license/PavelAndreyev1337/django-todo-react?color=green&style=flat-square)
![GitHub issues](https://img.shields.io/github/issues/PavelAndreyev1337/django-todo-react?style=flat-square)
## Using:
* Django
* DRF
* ReactJS

## How to run:
* `cd backend`
* `python -m venv venv`
* Linux - `source venv/bin/activate` Windows - `venv\Scripts\activate`  
* `pip install -r requirements.txt`
* change setting file `./backend/settings.py`:

        `DATABASES = {
            'default': {
                ....
            }
        }`

* `python manage.py migrate`
* `python manage.py runserver`
* `cd ../frontend`
* `npm install`
* `npm start`

## Deployment on VPS

* (optional) buy domain name
* connect to VPS
* add user `adduser newuser`
* add to sudo group `usermod -aG sudo newuser`
* ([optional](https://www.digitalocean.com/community/tutorials/c-ubuntu-16-04-ru)) Add an ssh key instead of a password
* `sudo apt-get update`
* `sudo apt-get install python3-pip`
* `sudo pip3 install virtualenv`
*  send the file using FTPS
*  create virtual environment `virtualenv venv`
*  activate environment `source venv/bin/activate`
* install dependencies `pip install -r requirements.txt`
* install nginx:
    * `sudo apt-get install software-properties-common` - add-apt-repository: command not found
    * `sudo apt-get update`
    * `nginx=stable`
    * `sudo add-apt-repository ppa:nginx/$nginx`
    * `sudo aot-get update`
    * `sudo apt-get install nginx`
* [configure]('https://medium.com/@timmykko/deploying-create-react-app-with-nginx-and-ubuntu-e6fe83c5e9e7) `nano /etc/nginx/sites-available/default`
* `sudo ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled`
* (optional) clear 80 port `sudo fuser -k 80/tcp`or find service `fuser 80/tcp` `ps -p <PID> -o comm=` and turn down service `sudo systemctl disable <service>` `sudo systemctl stop <service>`
* restart nginx `sudo systemctl restart nginx`
* change `ALLOWED_HOSTS = [...]`
* install gunicorn:
    * `pip install gunicorn`
    * configuration creation (create service) `sudo nano /etc/systemd/system/gunicorn.service`
    * `sudo systemctl start gunicorn`
    * `sudo systemctl enable gunicorn`
* add HTTPS [letsencrypt](https://certbot.eff.org/lets-encrypt/ubuntubionic-nginx).

[Live website](https://hqua0145494.online-vm.com/)

[Deployment tutorial.](https://pythonworld.ru/web/django-ubuntu1604.html)

Thanks for [tutorial](https://scotch.io/tutorials/build-a-to-do-application-using-django-and-react).

