## 아나콘다에서 PyQt 설치 및 업데이트
PyQt는 아나콘다 배포판을 설치하면 기본적으로 설치되는 패키지이다. 따라서 아나콘다 배포판 버전에 다라 설처된 PyQt 패키지 버전이 다를 수 있다.
1) 아나콘다 배포판에서 현재 설치된 패키지 목록을 확인하려면 conda list명령을 사용하면 된다. 참고로 conda list 명령 이후에 아무것도 입력하지 않으면 배포판에 설치된 모든 패키지의 정보가 출력된다.
PyQt 패키지에 대한 정보만 확인하려면 conda list pyqt를 입력하면 된다. 이때 패키지의 이름은 대소문자를 구분하지 않는다.

<center>
  <img src="https://github.com/kdahun/pyqt_relation/assets/101082485/6b4cc49e-039f-4f08-9e8a-fd8b1fd8f440">
</center>


## PyQt 시작하기
```
import sys
from PyQt5.QtWidgets import *

app = QApplication(sys.argv)

win = QWidget()
win.show()

app.exec_()
```

---
### 코드 분석하기
```
import sys
from PyQt5.QtWidgets import *
```
QtWidgets 모듈에는 QApplication 클래스가 정의되어 있다. 해당 클래스에 대한 객체를 생성한다. 이때 현재 소스 코드 파일에 대한 경로를 담고 있는 파이썬 리스트를 클래스의 생성자로 전달한다. PyQt5를 이용한 모든 프로그램은 반드시 QApplication 객체를 생성해야 된다.

```
app = QApplication(sys.argc)
```
생성된 QApplication 객체의 exec_ 메소드를 호출하여 이벤트 루프를 시작한다. 이벤트 루프가 시작되면 GUI 프로그램은 사용자가 닫기 버튼을 누를 때 까지 종료하지 않고 계속 실행된다. 이벤트 루프는 반복문 내에서 사용자로 부터 입력되는 이벤트를 처리하기 때문에 그 이름이 '이벤트 루프'인 것이다. 여기서 이벤트라는 것은 사용자가 마우스 클릭하거나 키보드를 입력하는 것과 같은 동작을 의미한다.

```
app.exec_() # 이벤트 루프 시작
```
이벤트 루프를 시작하기 전에 실제로 화면에 보여지는 윈도우에 대한 객체를 생성하고 이를 화면에 보여지도록 show 메소드를 호출해야 한다.
show 메소드를 호출하지 않으면 객체가 메모리에만 생성될 뿐 화면에는 보여지지 않게 된다.
```
win = QWidget()
win.show()       # 화면에 보여지게 한다.
```

---
### PyQt 위젯
```
import sys 
from PyQt5.QtWidgets import *

app = QApplication(sys.argv)

# ----------------- 수 정 ------------------
button = QPushButton("Button")
button.show()
# -------------------------------------------

app.exec_()
```
<img src="https://github.com/kdahun/pyqt_relation/assets/101082485/2bf69749-6cf4-4b97-9607-2ae38e38bdc0">


```
import sys 
from PyQt5.QtWidgets import *

app = QApplication(sys.argv)

# ----------------- 수 정 ------------------
label = QLabel("Label")
label.show()
# -------------------------------------------

app.exec_()
```
<img src="https://github.com/kdahun/pyqt_relation/assets/101082485/8766092a-ad1f-45e4-a113-d8905d9d09d8">


