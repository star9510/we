# 배전기자재 열화상진단 AI 분석모델

## 진단자의 숙련도에 상관없이 동일한 진단결과와 설비진단의 정확성과 신속성 향상을 위한 모델입니다.

### 프로젝트 인원: 5명
- 리더 : 배종태 - 분석모델 개발 총괄
- 팀원 : 윤석인 - 학습환경 구성
- 팀원 : 김영진 - 데이터 확보
- 팀원 : 정인권 - 알고리즘 구현
- 팀원 : 조민진 - 코칭

### 개발환경
- Python>=3.8.0 
- PyCharm Community Edition 2023.1 <https://www.jetbrains.com/pycharm/download/>
- yolov5 <https://www.bing.com/search?q=yolov5&qs=SC&pq=ㅛㅐㅣㅐ&sc=10-4&cvid=1626E86196E24F7F914B26A83A952436&FORM=QBRE&sp=1&lq=0>
- Thermal-Image-Analysis-master <https://github.com/detecttechnologies/Thermal-Image-Analysis>
- labellmg

### 주요개발내용
- labellmg 활용 열화상진단 사진자료 => 학습자료(TXT) 변환
- train.py labellmg 학습시행 EXP1~22 
- detect.py 열화상 진단사진 detecting 및 인식률 검증
- Thermal-Image-Analysis-master => main.py 열화상 온도 데이터 추출
- *dd_detect.py 개발 알고리즘 활용 설비detecting 및 온도 비교 불량 검출*

### 구동환경 세팅 
- 아래 3가지는 PyCharm Community Edition 2023.1/yolov5/Thermal-Image-Analysis-master 위 링크 혹은 첨부파일 자료 다운로드
- 진단 열화상 이미지는 "yolov5-master/datadiscovery/images" 에 위치

### 실행방법
- PyCharm Community Edition 2023.1 실행후 
- pip install logzero 설치 시행
- python dd_detect.py 시행

### 에러대처
- 만약 실행중 "ImportError:cannot import name 'scale_boxes' from 'yolo5.utils.general' 이 발생할경우 yolov5 버전이 달라서 함수값을 인식 못하는 경우로 scale_boxes => scale_coords 로 변경하면 실행 가능
- 위의 환경 세팅이 아닌 아나콘다, 주피터 실행시 별도의 tool 설치할 가능성 있음 
  
### 기타사항 
- 세부내용 및 진행은 첨부파일 내 동영상 참조
