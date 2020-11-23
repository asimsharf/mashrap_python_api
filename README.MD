docker build .
docker-compose build 
docker-compose run app sh -c "django-admin.py startproject app ."
docker-compose run app sh -c "python manage.py test"
docker-compose run app sh -c "python manage.py test && flake8" 
docker-compose run app sh -c "python manage.py startapp core"
docker-compose run app sh -c "python manage.py makemigrations core"
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/asimsharf/mashrap_python_api.git
git push -u origin main
                