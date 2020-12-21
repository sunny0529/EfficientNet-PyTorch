# EfficientNet-PyTorch

# Deept-ADDS
![image](https://user-images.githubusercontent.com/49579003/102768259-382c2400-43c4-11eb-8cf3-a2291fccc405.png)

- **ADDS** (Automatic Deepfake Detection System) - 딥페이크 자동 탐지 시스템

    영상 및 이미지의 **딥페이크 여부를 탐지하는 기술**을 토대로 사이버 상의 개인 얼굴 데이터 보호를 위한 서비스
    
    


![image](https://user-images.githubusercontent.com/49579003/102769971-bd183d00-43c6-11eb-90d6-54d550107615.png)
    **[모델 test 정확도]**

![image](https://user-images.githubusercontent.com/49579003/102769998-c5707800-43c6-11eb-91a5-0abeb4248053.png)
    **[Adversarial Attack 성공률]**

- **DEEP't**

    사이버보안 전공자 5명이 팀을 결성
    
    딥페이크의 등장과 악의적인 사용에 맞서, 더 나은 기술 개발하고자 한다.

## 모듈
- **django 관련**

    django 3.0.7

    django-storages 1.11

    django-rest-framework 3.12.2


- **django - s3 관련**

    boto3 1.16.40

    boto 2.49.0


- **딥페이크 판별 모듈 관련**

    future 0.18.2

    numpy 1.19.4 

    pillow 8.0.1 

    torch 1.5.1 

    torchvision 0.6.1

    opencv-python 4.4.0.46

    face-recognition 1.3.0
    
    tqdm 4.54.1

    matplotlib 3.3.3
 
    pandas 1.1.5

## 사용방법
**1. 가상환경 만들기**

    $python -m venv {가상환경 이름}

**2. 가상환경 실행**

    $source {가상환경 이름}/bin/activate

**3. 모듈 설치**

**4. Migrate 하기**

    $python manage.py migrate

**5. django 실행**

    $python manage.py runserver

## 실행화면

![로고페이지](https://user-images.githubusercontent.com/49579003/102734322-e7480b80-4382-11eb-9c91-974553083c0f.png)
    **[로고 화면]**

![사용법](https://user-images.githubusercontent.com/49579003/102734566-7f45f500-4383-11eb-9da5-3d30fe8a2f3e.png)
    **[사용법 동영상 화면]**

![딥페이크판별](https://user-images.githubusercontent.com/49579003/102734482-40b03a80-4383-11eb-8b98-afb58e955935.png)
    **[딥페이크 동영상/이미지 판별 화면]**
