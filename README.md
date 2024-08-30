# Start_Django_Project

#pour la creation d'un projet Django voilà les different etapes que nous effectuons jusqu'au lancement du server

1 - CREATION D'UN ENVIRONNEMENT VIRTUEL
#commande
python -m venv .env     #NB: .env est le nom de l'environnement virtuel
ensuuite
cd .env && cd Scripts && source activate

2 - INSTALLATION DE DJANGO et configuration

 #Installation de Django : 
 pip install django

#Création d'un nouveau projet Django : 
django-admin startproject projet   #ici notre projet creer es appelé projet

cd /projet

dans mons projet il y'aura dans l'aborescence de mon projet ceci:
projet/
    projet/
      __init__.py   #un fichier qui indique que ce fichier doit etre considéré comme un paquet
      setting.py    #Contient tous les configurations du projet
      urls.py        
      asgi.py       #déclarations des URL des application django qui serons creer
      wsgi.pi       #point d’entrée pour les serveurs Web
  manage.py         #utilitaire en ligne de commande pour lancer notre projet django

3 - CREER UNE APPLICATION
  python manage.py startapp blog   #blog le nom de mon application

  3 - 1 configuration de la base 

  ici en fonction de la base de donnée a utiliser nous installons un connecteur a l'aide de pip et dans le setting nous nous rendons dans DATABASES pour faire la suite des config
  
  3 - 2 configurations dans templates 
   a ce niveau nous nous rendons dans le meme fichier setting ensuite templates  on ajoute cette ligne 
   'DIRS': [BASE_DIR / 'templates'], pour faire reconnaitre tous les template dans nos applications

3 - 3 STATIC config
    on mets en bas de notre static cette ligne pour notre different projet static
    STATICFILES_DIRS = [ BASE_DIR / 'static/',]

3 - 4 lister ton application

dans INSTALLED_APPS de setting je liste blog

                                                                                          BLOG APPLICATION CREER


je creer un projet dans ce dossier un fichier urls.py pour les routes de cette application

dans l'aborescence du projet je creer egalement des dossiers notamment templates et static


 Lancer le serveur de développement  : 
 
 python monprojet/manage.py runserver


 bien avant le lancement on fait makemigrations pout la migrations de nos donnée
 python manage.py makemigrations   
 python manage.py migrate
 
  

