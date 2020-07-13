# ToDo application 

Using:
* Django
* DRF
* ReactJS

How to run:
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

Thanks for [tutorial]('https://scotch.io/tutorials/build-a-to-do-application-using-django-and-react').