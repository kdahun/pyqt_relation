# QPushButton
```
import sys
from PyQt5.QtWidgets import *

class MyWindow(QMainWindow):
  def __init__(self):
    super().__init__()
    self.btn = QPushButton("종료", self)
    self.btn.move(20,20)

app = QApplication(sys.argv)
mywindow = MyWindow()
mywindow.show()
app.exec_()
```

---
# QPushButton 시그널
```
import sys
from PyQt5.QtWidgets import *


class MyWindow(QMainWindow):
    def __init__(self):
        super().__init__()

        self.btn = QPushButton("종료", self)
        self.btn.move(20, 20)
        self.btn.clicked.connect(self.btn_clicked)

    # 버튼이 클릭될 때 호출되는 메서드
    def btn_clicked(self):
        self.close()

app = QApplication(sys.argv)
mywindow = MyWindow()
mywindow.show()
app.exec_()
```

---
# QPushButton 크기 조절
버튼 객체의 resize 메서드를 사용해서 버튼의 크기를 조절할 수 있다.
```
btn = QPushButton("종료",self)
btn.resize(100,10)
```

---
# QPushButton 활성화
```
btn = QPushButton("종료",self)
btn.setEnabled(True)  # 활성화
btn.setDisabled(True) # 비활성화
```

---
# QPushButton 텍스트
text 메서드를 통해 버튼의 텍스트 값을 얻어올 수 있다.
```
btn = QPyshButton('button', self)
print(btn.text())
```


