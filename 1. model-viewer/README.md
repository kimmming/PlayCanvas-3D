# ModelViewer - PlayCanvas Tutorial

[Publishing at PlayCanvas](https://playcanv.as/b/e8c0b298)

ModelViewer는 PlayCanvas 를 사용하여 3D 모델을 엡에서 렌더링하고 조작하는 방법을 보여주는 예제 프로젝트입니다.
 이 프로젝트는 3D 모델의 로딩, 디스플레이, 카메라 조작, 기본 조명 및 재질 설정 등의 기능을 다룹니다.

 ## 실행 방법
1. [ModelViewer](https://playcanvas.com/editor/project/1153963) 프로젝트의 Editor를 열어 어떤 HIERARCHY 패널을 확인합니다.
   해당 패널은 프로젝트 내의 모든 엔티티와 그들의 계층 구조를 보여줍니다.
2. HIERARCHY 내에서 'Camera' 엔티티를 찾습니다. 이 카메라 엔티티는 사용자가 3D 모델을 보는 데 사용되는 주요 뷰포인트입니다.
3. 'Camera' 엔티티를 선택한 후, INSPECTOR 패널에서 카메라의 속성을 조정할 수 있습니다. 여기서 카메라의 위치, 회전, 필드 오브 뷰(FOV) 등을 설정할 수 있습니다.
4.  HIERARCHY에서 'playcanvas' 엔티티 찾아 선택합니다. 이 엔티티는 화면에 표시될 3D 모델을 나타냅니다.
5.  INSPECTOR 패널에서 'playcanvas' 엔티티의 속성을 조정할 수 있습니다. 여기서 엔티티의 위치, 크기, 회전 및 사용된 재질 등을 설정할 수 있습니다.
6. 상단의 툴바에서 'Play' 버튼을 클릭하여 프로젝트를 실행합니다. 이 버튼을 누르면 새 브라우저 탭이 열리고 프로젝트가 로드됩니다.
7. 브라우저에서 프로젝트가 실행되면, 마우스나 터치스크린을 사용하여 카메라를 조작하고 3D 모델을 다양한 각도에서 볼 수 있습니다. 마우스의 좌/우 버튼이나 휠, 키보드 입력 등을 통해 인터랙션할 수 있습니다.

이 과정을 통해 ModelViewer 프로젝트를 실행하고, 3D 모델을 웹 브라우저에서 실시간으로 뷰잉하고 인터랙션하는 방법을 경험할 수 있습니다.

## 스크립트
PlayCanvas ModelViewer 프로젝트에서 스크립트는 주로 카메라 조작, 모델 로딩 및 렌더링, 사용자 인터랙션 처리 등을 담당합니다. 


### 1. OrbitCamera 
- 'OrbitCamera' 스크립트는 카메라의 움직임을 관리합니다. 이 스크립트는 사용자가 3D 모델 주변을 자유롭게 회전하고 확대/축소할 수 있게 해줍니다.
-  'Camera' 엔티티에 'OrbitCamera' 스크립트를 추가합니다.
- 스크립트 속성에서 회전 감도, 최대/최소 거리, 피치 각도 등을 조정합니다.

### 2. Input 
- 터치 및 마우스 입력을 처리하는 'TouchInput'과 'MouseInput' 스크립트를 추가합니다. 이 스크립트는 사용자의 입력에 반응하여 카메라를 조작합니다.
