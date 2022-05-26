# EraofConquest
Youtube: https://youtu.be/YVrjGD6Zvns

GoogleSpreadsheets: https://docs.google.com/spreadsheets/d/1L2FWK8NyCipB0KA-n64m0UNP8RZroxDGt7zicYdNjv8/edit#gid=1012642768

# 개요
1. 장르
캐쥬얼, RTS, 전략
2. 컨셉
3D타일맵 RTS
2. 플랫폼
PC window기반
3. 타겟플레이어
RTS게임이지만 캐쥬얼한 그래픽과 쉬운 조작법으로 10~20대의 젊은 층을 생각했습니다.
4. 전체클래스 구성


# 기술요소
1. 행동트리
유닛 AI 클래스다이어그램 및 시퀀스 다이어그램
![image](https://user-images.githubusercontent.com/37317856/170419291-a55954ff-b940-40c7-a463-b578bed2f87f.png)
초기에 FSM기반 상태 전이를 이용하였으나 인공지능 수업에서 BT를 접하고 이를 이용하여 재구성하였음 
![image](https://user-images.githubusercontent.com/37317856/170419725-d85d811e-e5a8-4d07-8b71-883df6320bb8.png)
AI의 Update에 있던 다양한 기능들을 모듈화가 가능하여
2. ScriptableObject활용
플레이어 및 적 팩션데이터, 튜토리얼을 위한 다이얼로그,유닛 및 건물에 사용되는 변수들을 클래스단위로 묶어 저장후 불러오기가능
3. excelImporter
엑셀로 DB화하여 저장한 데이터들을 scriptableObject로 꺼내 사용
4. GoogleSpreadsheet
execelImporter를 활용해 만든 Excel SO를 GoogleSheet에서 업데이트해 사용
게임 시작시 구글시트에 데이터들을 불러와 사용하기때문에 빌드후 데이터 수정에도 용이함

