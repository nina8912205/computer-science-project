# 201911884 응용통계학과 정예원 - 다전공 프로젝트




## I . 다전공 신청 동기

   2학년 1학기에 응용통계학과 전공강의 '탐색적자료분석'을 듣고 코딩에 흥미를 느꼈습니다. 또한 빅데이터 분석가가 되기 위해서는 통계적 역량 뿐만 아니라, 코딩 역량도 필요하다는 것을 깨달았습니다. 그래서 작년 여름방학에 '점프 투 파이썬(박응용 저)' 교재로 파이썬을 독학했습니다. 교재를 마친 뒤, 이론적 코딩 지식 뿐만 아니라, 코딩 응용능력을 길러야 겠다고 생각했습니다.



  그래서 코딩 테스트를 통해 응용통계학과 내 머신러닝 동아리 'KUGGLE'에 들어가게 되었습니다. KUGGLE에서 KNN, 앙상블, Crawling 등을 배웠습니다. 하지만, 파이썬 기초 능력 밖에 없던 저에게는 다소 어렵게 느껴졌습니다. 동아리에서 조차 쉽게 채워질 수 없는 ‘컴퓨터적 사고의 기초’를 배울 필요성을 느꼈습니다.



  많은 고민을 하며 교수님과 선배님들과 많은 상담을 한 끝에 저는 컴퓨터공학부를 다전공하여 보다 깊이 있게 데이터 분석 툴을 공부 해야겠다고 결심했습니다. 코딩의 기초를 탄탄하게 다질 수 있는 가장 좋은 선택지는 ‘컴퓨터 공학부 다전공’이라고 생각했습니다.







## II . 프로젝트 구상


![포스](https://user-images.githubusercontent.com/71542788/104808531-3c642980-582a-11eb-8764-0b32d7615963.png)

저는 지금까지 프로젝트 경험이 없었습니다. 그래서 다전공 신청을 위해 처음으로 프로젝트를 진행해 보았습니다. 사실상 코딩 경력이라곤 ‘점프투파이썬 교재 완독’ 이 전부인 상태였습니다. 파이썬 언어로 구현할 수 있는 것들을 찾아보다가, gui를 알게 되었습니다. 데이터를 바탕으로 컴퓨터와 인간이 소통하게 끔 한다는 점에서 gui가 흥미로웠습니다.



또한, 저는 재 작년 아쿠아리움 푸드코트에서 아르바이트를 해 본적이 있습니다. 포스기에서 주문을 받을 때 사용한 주문 시스템이 gui가 아니었을까 생각했습니다. 저와 같은 알바생인 유저가 시스템을  쉽게 이용하도록 프로그램을 짠다는 것이 재미 있어 보였습니다. 그래서 제가 아쿠아리움에서 알바하며 사용했던 프로그램과 비슷하게 음식 주문 gui를 구현해보기로 결정하였습니다.







## III . 프로젝트 과정

-     저의 프로젝트는 (2020. 12. 29 ~ 2021. 01. 14) 약 2주간 걸쳐 진행되었습니다.


### (1)  프로젝트 전 학습

프로젝트를 위해서 유튜브와 책을 통해 파이썬을 다시 공부하고, Gui에 대해 공부했습니다. 하단(V . 프로젝트 중 참고자료 및 공부자료)의 유튜브 영상을 보며 코드를 하나하나 따라치며 파이썬을 상기했습니다. 무엇보다 유튜브 영상의 프로그램들을 보며 “gui 기능을 나의 프로젝트에 어떻게 적용할 수 있을지” 고민하며 공부했습니다.





### (2)  학습 후 프로젝트 과정


#### ①    양식 선택 – radiobutton, button



![버튼](https://user-images.githubusercontent.com/71542788/104808427-957f8d80-5829-11eb-964b-394d4f5ac1e0.png)



  우선, 햄버거, 사이드메뉴, 음료 선택부분은 radiobutton으로 설정해 보았습니다. 제가 학습한 양식 중 메뉴 선택에 가장 적절하다고 생각했기 때문입니다. Radiobutton은 첫 화면에 메뉴 전체가 사용자에게 보이게 하고, value값을 지정할 수 있어 주문에 따른 가격 계산을 하는 데 용이할 것이라고 생각했기 때문에 적절하다고 판단했습니다.


  반면,  button은 메뉴 선택보다는 주문실행에 적절하고, checkbox는 값이 0과 1로 지정되어 다양한 메뉴에 각각 다른 값을 부여하는 데 한계가 있다고 판단했습니다. 다만, checkbox는 ‘피클제거’ ‘치즈추가’ 등과 같이 추가적인 요구사항을 체크하는 데 쓰일 수 있겠다고 생각했습니다.
  
  
  
 
 
#### ②   메뉴 데이터 설정 – crawling 





![버거](https://user-images.githubusercontent.com/71542788/104808451-c495ff00-5829-11eb-8ad4-221fdbb5a480.png)



처음에는 메뉴 이름과 가격을 제가 임의로 설정했습니다. 임의로 설정된 메뉴 이름과 가격을 바탕으로 message box를 통해 총 주문 가격을 사용자에게 알리고, 출력하는 프로그램을 짰습니다. 하지만, 프로그램을 짜고 보니 제가 지정한 데이터 보다, 실제 프렌차이즈 가게의 메뉴 데이터를 크롤링하면 실제 체인점에서 이용하는 포스기 프로그램과 더욱 비슷할 것이라고 생각했습니다.



  그래서 동아리 ‘Kuggle’에서 배운 crawling내용을 다시 공부한 후, 롯데리아 홈페이지의 햄버거, 디저트, 드링크 메뉴의 데이터를 크롤링했습니다. radiobutton의 각 value에는 메뉴의 가격을 할당했습니다.



  롯데리아로 크롤링을 한 이유는 롯데리아 홈페이지가 다른 프렌차이즈 홈페이지보다 파싱이 간단했기 때문입니다. 예를 들어, 맘스터치 홈페이지 같은 경우, 메뉴 이미지를 클릭해야 지만 메뉴의 가격과 칼로리 등을 볼 수 있습니다. 하지만 롯데리아는 메뉴이름, 칼로리, 가격이 같은 페이지에 동일한 패턴으로 적혀 있어 파싱이 간단했습니다.
  
  
  
  

#### ③   주문하기 버튼 – 함수 적용



![버튼2](https://user-images.githubusercontent.com/71542788/104808462-d5df0b80-5829-11eb-9214-506ea436a76c.png)


주문하기 버튼에는 order 함수를 적용했습니다. order함수에는 선택된 햄버거, 사이드 메뉴, 음료의 value 값인 가격을 합한 값을 message box에 표시하고, 주문금액이 맞는지 사용자에게 알려주고 출력하는 기능을 부여했습니다. If else 구문을 활용하여 주문금액이 예상과 다른 경우, 주문 철회를 할 수 있도록 했습니다.





#### ④    한계점 시정 – listbox, button(주문취소, 주문추가), radiobutton(주문안함)




![주문가격](https://user-images.githubusercontent.com/71542788/104808459-d1b2ee00-5829-11eb-9bc1-cd136804cac4.png)
![주문확인](https://user-images.githubusercontent.com/71542788/104808460-d24b8480-5829-11eb-9b9c-8c17bc2b7056.png)
![경고](https://user-images.githubusercontent.com/71542788/104808467-dbd4ec80-5829-11eb-8ab1-c71c4378f555.png)



  위와 같은 과정으로 [ 햄버거,사이드메뉴,음료 선택 -> 주문하기 버튼 -> message box로 총 주문금액 확인 ] 과 같이 동작하는 프로그램을 만들었습니다. 하지만, 생각해보니, radiobutton은 무조건 메뉴 하나는 선택되기 때문에 제 프로그램에서는 사용자가 세 종류의 메뉴 중 두 종류, 또는 한 종류 만 주문할 수는 없다는 것을 알았습니다. 또한, 햄버거, 사이드 메뉴, 음료 세 가지를 한 번에 하나 씩만 주문하는 것이 아니라, 각각 다른 개수를 여러 개 주문하지도 못한 다는 것도 깨달았습니다.



  그래서 각 label에 radiobutton ‘주문안함’을 추가했고, value 값을 0으로 지정하여 반드시 세 종류를 다 주문하지 않아도 되도록 했습니다. 또한, 주문 label 위에 listbox를 만들어, 사용자가 주문을 계속 추가할 때 마다 listbox에 주문가격이 추가되도록 했습니다. 반대로, listbox에서 선택한 항목은 주문 선택 취소를 하도록 취소버튼을 만들었습니다. 그래서 총 주문가격을 burger_var.get()+side_var.get()+drink_var.get() 대신, listbox에 책정된 가격을 합산한 값으로 인식하도록 했습니다.



  또한, 사용자가 아무것도 주문하지 않을 경우, 총 주문금액이 0으로 출력되지 않도록, 주문 메뉴를 선택하라는 경고창도 추가했습니다.
  
  
  
  
  
  

## IV . 프로젝트 후 느낀점

  Gui를 만들 때, 프로그램을 이용하는 주체는 시스템 유저이기 때문에, 코드를 짜는 과정에서도 유저의 입장에서 동작하기 편하도록 코드를 작성해야 한다는 것을 깨달았습니다. 그 과정에서 개발 전공자만 알 수 있는 어려운 코드 보다는 보다 간결하고 깔끔한 코드가 좋은 코드라는 것을 알았습니다. 제 입장보다는 프로그램을 처음 접하는 사람이 이해하기 쉽도록 코드를 계속 수정했습니다.



  그런 점에서 제 코드는 몇 가지 부족한 점이 있다고 생각했습니다.

  먼저, 추가된 주문 listbox에 가격만 기입되어서 사용자가 주문한 메뉴의 이름을 확인할 수 없습니다. Listbox에 추가된 주문 메뉴들의 가격을 다 더한 값을 출력하려다 보니, 문자형인 주문 메뉴 이름을 기입할 수 없었습니다. 저는 문자형과 숫자형이 listbox에 혼합 되어있을 때 숫자형만 추출하여 연산하는 것은 도저히 모르겠어서 가격만 listbox에 표시되도록 했습니다. 주문 목록에 주문 메뉴 이름까지 명시했다면, 사용자가 주문 목록을 잘 체크할 수 있었을 것이라고 생각했고, 이 점에서 제 코드가 매우 아쉬웠습니다.



  또한, 체크박스를 통해 ‘피클제거’, ‘치즈추가’ 등의 선택요소를 추가하려고 했지만, 역시 숫자형인 총 주문 금액과 문자형인 주문메뉴 및 선택사항을 함께 처리하는 방식을 찾아내지 못해 코드를 짜지 못했습니다. 이 점 역시 매우 아쉬웠습니다.



  아쉬운 점이 많았지만, 배우고 느낌점은 더 많습니다. 다전공 신청을 위해서 진행한 프로젝트였지만, 프로젝트를 하면서 어느때보다 파이썬 실력이 신장됨을 느꼈습니다. 코딩은 개념 공부도 중요하지만, 다양한 시도를 하며 창작물을 만드는 과정에서 실력이 는다는 것을 깨달았습니다. 또한, 진정한 실력자가 되기 위해서는 단순히 코딩지식을 많이 아는 것 보다는 풍부한 창의력을 바탕으로 기술을 다채롭게 이용할 수 있는 능력이 중요하다는 것을 알게 되었습니다.



  컴퓨터공학부를 다전공하며, 컴퓨터적 사고와 코딩의 기초를 탄탄히 다지고, 저의 원전공과 결합하여 더욱 풍부한 창의력을 발휘하겠습니다. 다전공을 하며 전공 공부는 물론이고, 다양한 프로젝트와 공모전에 참가해 실질적인 실력을 쌓겠습니다. 통계적 사고를 바탕으로 코딩이라는 도구를 가지고 전문 분야에서 활약하는 빅데이터 분석가가 되겠습니다.







## V . 프로젝트 중 참고자료 및 공부자료

https://www.youtube.com/watch?v=kWiCuklohdY   & 점프투파이썬(박응용 저)  -> 파이썬 복습

https://www.youtube.com/watch?v=D8-snVfekto&t=1967s    -> gui 공부

https://www.youtube.com/watch?v=bKPIcoou9N8&t=9797s    -> gui 공부




