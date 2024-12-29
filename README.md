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