# north_pole

1. **기간 : 2021.04~2021.04** 

2. **기술스택 : python, pandas, numpy, tensorflow, keras** 

3. **내용 : 북극의 과거 482개월간의 이미지를 보고 향후 24개월의 이미지를 예측하기**  
    1. 이미지 데이터를 pickle파일로 변환  
    2. 2차원 픽셀 이미지를 flatten 및 정규화  
    3. 직전 7개월의 이미지를 가지고 향후 1개월의 이미지를 예측  
    4. sliding window를 이용해 점진적으로 학습 및 예측  

4. **파일설명**  
    1. dataToPickle.ipynb (input : train폴더, output : dataP). 
        - train폴더에 있는 이미지 데이터를 피클파일로 전처리하여 dataP폴더에 저장. 
    2. model1_lstm.ipynb (input : dataP, output : sub_1.csv, sub.pickle). 
        - 피클파일을 input으로 받아 lstm을 이용하여 학습  
        - 결과값 피클로 저장  
        - sample_submission 이용하여 dataframe형성  
        - 결과 피클값을 dataframe에 적용하여 제출파일(sub.csv)형성  
        - models폴더에 모델 10에포크마다 저장  
