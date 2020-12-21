# EfficientNet-PyTorch

# Deept-ADDS
![image](https://user-images.githubusercontent.com/49579003/102768259-382c2400-43c4-11eb-8cf3-a2291fccc405.png)

- **ADDS** (Automatic Deepfake Detection System) - 딥페이크 자동 탐지 시스템

    영상 및 이미지의 **딥페이크 여부를 탐지하는 기술**을 토대로 사이버 상의 개인 얼굴 데이터 보호를 위한 서비스
   
- **기술 요약**

    기본적인 딥페이크 디텍션(Open CV를 활용한 얼굴 탐지/Xception Net을 활용한 딥페이크 판별)에 Adversarial Example Training(FGSM)으로 강화된 딥페이크 디텍션을 제공한다. 학습에 사용된 데이터는 ‘FaceForensic’,‘Kaggle’,’DeeperForensic’으로 총 400GB 상당의 3가지 데이터셋을 활용했다. 해당 딥페이크 디텍션 모듈을 이용할 수 있는 웹을 제공한다.
    
- **모델 성능**

    [모델 test 정확도]

    ![image](https://user-images.githubusercontent.com/49579003/102771009-71669300-43c8-11eb-867e-c85ca9c31d54.png)

    [Adversarial Attack 성공률]

    ![image](https://user-images.githubusercontent.com/49579003/102769998-c5707800-43c6-11eb-91a5-0abeb4248053.png)

- **DEEP't**

    사이버보안 전공자 5명이 모여 팀을 결성했다. 딥페이크의 등장과 악의적인 사용에 맞서, 더 나은 기술 개발하고자 한다.
    
## 모듈
- **django 관련**

    django 3.0.7

    django-storages 1.11

    django-rest-framework 3.12.2


- **django-S3 관련**

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

## 실행 방법
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

![image](https://user-images.githubusercontent.com/49579003/102774069-9c071a80-43cd-11eb-81b4-71c64972afb8.png)

**[결과 화면]**


## 웹 개발 과정
- **django 환경 구축**

    2020.07.01 django-파이썬 연동 확인/SQL 연동
- **데이터베이스(S3) 연동**
- 2020.07.17 S3 계정 만들기/django-S3 연동
- 2020.07.20 S3 이미지 업로드/보여주기 완료
- 2020.07.27 S3 동영상 업로드 완료

    업로드시 소리만 나오는 문제 해결 (인코딩/imgfield에서 filefield로 변경)
- **동영상 보여주기**
- 2020.09.03 동영상 플레이어
- 2020.09.04 동영상 플레이어-S3 연동

    S3에 동영상 업로드 후 객체 url을 받아와 동영상 플레이 완료
- **2020.09.06 전체적인 백엔드 기능 개발 완료**
- **ADDS 딥페이크 모듈-django 연동**
- 2020.09.07 파이썬 함수에서 변수 넘겨받기 완료
- 2020.10.24 딥페이크 모듈의 결과 값인 Bounding Box 동영상 띄우기 완료
- 2020.11.17 딥페이크 모듈-django 연동
- 2020.12.02 딥페이크 모듈의 결과 값인 그래프 이미지 띄우기 완료

- **2020.09.07 클라우드 서버(E2C) 배포**

## 웹 남은 이슈
- 딥페이크 탐지 결과를 기다리는 동안, 사용자가 업로드한 동영상을 보여주기
- S3에 업로드한 이미지/동영상에 다시 접근시 권한 문제
- 보안
