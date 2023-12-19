
Dockerfile oluşturduktan sonra aşağıdaki docker kodu ile docker image oluşturdum.

     docker build -t web-app-image .


Deployment için .yaml dosyasını oluşturdum ve .yaml dosyasını kullanarak kubernetes ile deploymentı oluşturdum.

    kubectl apply -f web-app-deployment.yaml


Aşağıdakı komut ile ReplicaSetin çalıştığını kontrol ettim.

    kubectl get rs

ClusterIP tipi Servis için "web-app-service.yaml" dosyasını oluşturdum. Bu dosyayı kullanarak servisi oluşturdum.

    kubectl apply -f web-app-service.yaml


Servisin IP adresini bulmak için aşağıdaki komutu kullandım.

    kubectl get svc web-app-service

Terminal çıktıları: 
![image](https://github.com/LOG-IN-DEVOPS-BOOTCAMP/kubernetes-assignment-1-IkbalKulahcioglu/assets/65568713/08719442-d33d-4080-baf0-9803f9c37749)
