# Graduation-Project

•	게임 시퀀스 제작 : 타이틀 -> 튜토리얼 -> Stage1 -> Stage2 -> Boss Stage
•	사용자 인터랙션 : Ctrl(앉기), Space(점프), LMB(사격), RMB(저격총일 경우 줌모드)
•	레벨 디자인 : Stage1에서 적의 수가 적고 장거리 사격 위주로 플레이, Stage2에서는 적의 수와 종류가 늘어나며 근거리 위주로 달려옴으로써 난이도 상승, Boss Stage에서 보스의 체력과 공격력이 매우 높음. Stage 단계별로 난이도가 상승하는 것으로 레벨 디자인 적용
•	사용자 인터페이스 및 사운드 : 미니맵, 현재 총, 남은 총알, HP바를 Ui에 표현하였고 미션 완료를 위해서 어떻게 해야하는지 창도 띄웠습니다. 사운드는 BGM과 피격, 사격, 공격 등 여러 효과음을 적용 했습니다.	

•	Character : 적과 플레이어의 기본 스탯을 ScriptTableObject 로 구성하였고 캐릭터들의 데미지를 받고 HP 감소 및 증가에 대해 겹쳐지는 부분과 죽었을 때 서로 작용하는 부분이 달라 virtual, override 를 통해 오브젝트들의 상속 코드 작성
•	Weapon : 근접 공격, 원거리 공격 모두 기본적인 것을 부모 자식 간의 설정으로 코드 재 사용성을 높였으며 근접, 원거리 모두 RayCast 방식을 사용
•	Minimap : Player 의 위치를 기준으로 Enemy 의 위치를 계산하고 그에 따른 미니맵 Ui 이미지를 배치하여 미니맵 상에 보여지게 코드 작성
•	Stage Controller : Stage 마다 주로 하는 목표와 목표물 등이 달라지기에 기초적으로 공통되는 부분을 부모 클래스에 넣어두고 상속을 하여 스테이지 별 달라지는 것들을 override 로 구성하여 구현
•	Enemy : Behavior Tree 에디터를 사용하여 기본적으로 주어지는 노드들을 이용하고 필요한 기능의 노드를 코딩을 하여 적의 종류마다 다른 패턴을 구현
•	Boss : Behavior Tree 에디터를 이용하여 점프 공격, 돌진 공격, 산성 침 뱉기 총 3 가지 패턴을 구현하였고 각 패턴마다 콜라이더를 따로 둬서 패턴이 시작했을 때 SetActive 를 True 로 끝났을 때는 False 로 바꿔가며 플레이어에게 데미지를 줄 수 있도록 구현
•	Game Stop : deligate 를 사용하여 게임을 멈추고 다시 시작할 때의 필요한 것을 담아서 한번 호출로 여러 개의 함수를 호출 할 수 있도록 구현

youtube 링크 : https://www.youtube.com/watch?v=7N_C8KMS3Q8&list=PLKXf0qhZKKaewCYZaOvtjjkJeuhTCj6Qq&index=1
