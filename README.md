# Task Submitted to YottaByte

## The Task Utilizes Minikube on a Ubuntu VM.

### Pre-reqs Performed.

- Installed Docker
- Installed Virtual Box & Extensions
- Installed Minikube
- Install Kubectl

### Step :1  New User Created

- Created a user named `ahsan` & gave permissions to run docker
- Password for that user if needed is `!!!Lego2014!!!`

### Repo content
- Index.html to be used as a webpage.
- Dockerfile contains build information of the image using alpine.
- `app.yml` is the simple app deployment file
- `service.yml` is a service load balancer.

### Process Involved 

##### Starting MiniKube
- The contents of git reside in /opt/yotta/
- cd to that directory & run `docker build -t yotta .`
- I've pushed this image to my personal docker hub account & kubectl is using that one. `https://hub.docker.com/repository/docker/ahsan75/yotta`

##### Starting MiniKube
- `minikube start`
- `kubectl apply -f app.yml` &  `kubectl apply -f service.yml`
- `minikube tunnel` to expose external IP Address
