# 가상 환경 설정
conda env create -f environment.yml 
conda activate guidegan

# 데이터셋 경로 설정
trainA, trainB, testA, testB를 subfolder로 가지고 있는 데이터셋 폴더 경로가 './Dataset_sample/BDD100K/Night2Day'라고 한다면
./options/base_options.py 내 line 24의 "--dataroot"를 './Dataset_sample/BDD100K/Night2Day'로 설정
(현재는 데이터 샘플로 실행할 수 있게 설정해놓은 상태)

# 학습 코드 실행
python train.py
--> ./checkpoints/GuideGAN 폴더에 학습 weight 저장

# 테스트 코드 실행
python test.py
--> results 폴더 내에 결과 이미지 저장

# 결과 이미지
**Day → Night Task (Real/CycleGAN/Proposed)**
![image](https://github.com/user-attachments/assets/2639e92b-ee85-4020-baad-c0cdf7063a41)
![image](https://github.com/user-attachments/assets/bed2f178-2818-4046-b3d5-8b9b84a71b16)
![image](https://github.com/user-attachments/assets/03ece2f1-4235-4222-96e5-568bd0b8a2c0)

**Night → Day Task (Real/CycleGAN/Proposed)**
![image](https://github.com/user-attachments/assets/a6cd4933-d95d-4148-8f6c-2a36be333e2e)
![image](https://github.com/user-attachments/assets/4a257faf-325c-44cf-81c2-ffbb29f6bb9c)
![image](https://github.com/user-attachments/assets/3c6bc4a1-f0a1-477a-8cae-f367fc8a8e76)
