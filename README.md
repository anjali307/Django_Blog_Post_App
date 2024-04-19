## Running the Project Locally

First, clone the repository to your local machine:

```bash
git clone https://github.com/anjali307/Django_Blog_Post_App.git
```

Install the requirements:

```bash
pip install -r requirements.txt
```

Create the database:

```bash
python manage.py migrate
```

Finally, run the development server:

```bash
python manage.py runserver
```

The project will be available at **127.0.0.1:8000**.

## Running the Project With EC2 and Docker.

In this project you ca find DockerFile and Docker.compose file

1) Create Ec2 Instance and connect that with SSH.
2) Go to the rrot directory which is blog_post_app in that you can see Dockerfile.
3) Create Docker image using below command.
   
```bash
docker build -t mynewapp .
```

4) Create docker container
   
```bash
docker run -d -p 8000:80 mynewapp
```

Now this project will be available at **<Public_Ip-address_of_Ec2>:8000**.

