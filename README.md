# django-todo
A simple todo app built with django

![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)
### Setup

Create a EC2 instance of ubuntu of instance type of t2.micro in AWS

Edit inbound rules:
    Add Security Rules:
      Create a Custom TCP of Port Range 8000 with source of Anywhere IPv4.

Now Connect the instance.
Update the instance
```bash
  sudo apt update
```

To get this repository, run the following command inside your git enabled terminal
```bash
git clone https://github.com/0mchoudhary/Django_todoApp_EC2.git
```

Change the permission of directory
```bash
chmod 777 Django_todo_EC2/
```

Install Python command-line applications with pip in isolated virtual environments
```bash
sudo apt install pipx -y
```

Create a lightweight virtual environment 
```bash
python3  -m venv venv
```

Activate the virtual environment
```bash
source venv/bin/activate
```

Change the directory
```bash
cd Django_todo_EC2/
```

You will need django to be installed in you computer to run this app.
```bash
 pip install django
```

Once you have downloaded django, go to the cloned repo directory and run the following command

```bash
python3 manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
python3 manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user
```bash
python3 manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
python3 manage.py runserver 0.0.0.0:8000
```

Once the server is hosted, head over to http://YOUR_INSTANCE_IP_ADDERSS:8000/todos for the App.

Cheers and Happy Coding :)
