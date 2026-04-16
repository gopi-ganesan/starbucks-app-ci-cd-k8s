step 1:
    build the docker image 
step 2:
    helm install my.chart --namespace starbucks-ns --create-namespace
step 3:
    create a own helm template name an my-chart
step 4:
    add the mongodb statefulset and service template in my-chart
step 5:
    crate jenkins file for ci/cd pipeline
step 6:
    install in ec2 instance SonarQube using Docker and jenkins 
    command :
         sudo apt-get update
         sudo apt-get install docker.io
         sudo systemctl start docker
         sudo systemctl enable docker
    sonarqube installation command :
         docker run -d \
         --name sonarqube \
         -p 9000:9000 \
         sonarqube:lts
    jenkins installation command :
        sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
        https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key
        echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
        https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
         /etc/apt/sources.list.d/jenkins.list > /dev/null
        sudo apt update
        sudo apt install jenkins
        sudo apt update
        sudo apt install fontconfig openjdk-21-jre
        java -version 
        (or)
        docker run \
       --name jenkins-blueocean \
       --restart=on-failure \
       --detach \
       --network jenkins \
       --env DOCKER_HOST=tcp://docker:2376 \
       --env DOCKER_CERT_PATH=/certs/client \
       --env DOCKER_TLS_VERIFY=1 \
       --publish 8080:8080 \
       --volume jenkins-data:/var/jenkins_home \
       --volume jenkins-docker-certs:/certs/client:ro \
       myjenkins-blueocean:2.541.3-1
step 7:
    
# starbucks-app-ci-cd-k8s
# starbucks-app-ci-cd-k8s
# starbucks-app-ci-cd-k8s
# starbucks-app-ci-cd-k8s
