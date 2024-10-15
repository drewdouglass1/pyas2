Simple steps to create running pyas2 container
Create new Project directory

python -m venv dev

source dev/bin/activate

pip install django-pyas2

django-admin startproject tgcs_pyas2 .

update urls.py based on docs, update settings.py based on docs plus add without quotes - "from django.conf.urls import include"

#Run command below to create the initial pyas2 config/setup
python manage.py migrate

#Run command to create admin user. This creates the user manually in the db.sqlite3
python manage.py createsuperuser

podman build --tag pyas2:v1 .
