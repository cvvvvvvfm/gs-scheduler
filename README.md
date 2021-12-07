# GE-Global Scheduler
## Multiple Cluster 적용을 위한 버전으로 gedge scheduler 기능 확대 
- 다수 개의 Edge Cluster / Cloud Cluster 을 Target Cluster로 적용  
- Center Management Cluster와 통합 
## Developing Test System  
![develop_sys](https://user-images.githubusercontent.com/74521072/144995753-4aca9a88-45aa-45d9-95e6-2d319b841a81.png)
## GE-Global Scheduler : Core Modules
![core_m](https://user-images.githubusercontent.com/74521072/144995746-1a6e7a32-7c20-440b-a8e1-12448f9ab36a.png)
## GE-Global Scheduler 요청 작업 Request Queue 3Level로 관리   
- 빠른 처리를 위한 Fast Option 적용을 위한 특수 Queue 적용
- Request Queue Lifecycle을 통한 효율적인 관리
## GE-Global Scheduler Prewarmer 기능 제공
- Request Queue을 처리 요청 규모에 따른 빠른 처리를 위해 Prewarming 기능 제공
- Request Policy Queue에 따른 ScalUp/Down이 가능하도록 개발 
## Service External IP 제공
- 각 cluster에 Metallb 서비스 적용 
## Storage Service을 위한 Storage Server 운용 
- Center Management Cluster에 NFS Server 적용 
- Dynamic Volume Provisior 제공 
- Dynamically Provision NFS Persistent Volumes 제공
## 다양한  Data Storage Service 제공 
- Memory 기반 Redis 서비스 제공  
- Meta Data Storage을 위한 MongoDB Service 제공 
## Cluster들 간에 Message Service을 위한 Message Server 운용 
- Center Management Cluster에 Kafka Server 적용 
-  1:N, 1:1 Message 서비스 제공 
## GE-Local Scheduler 관련 모듈 모두 POD로 작동  
- Cluster Agent POD
- Worker Agent POD 
- Local Scheduler POD
## GE-Global Scheduler System Structure
![system](https://user-images.githubusercontent.com/74521072/144995738-ee675fbc-8097-46a8-8d11-292a37dfba9a.png)
## 새로운 스케줄러 정책 추가 
- (G)MostRequestedPriority
- (G)LowLatencyPriority
- GSelectCluster 

