# FORM

### Index Page
[https://yo-onhye.github.io/00.web-accessibility/01.form/form_index.html](https://yo-onhye.github.io/00.web-accessibility/01.form/form_index.html)

### 1) TEXT FIELD
* 애니메이션 사용
* aria-live 사용해서 develope해보기


**input type="number" vs input type="tel"**

| 구분 | input type="number" | input type="tel" |
| :---: | :---: | :---: |
| maxlength | maxlength 속성 미지원 | maxlength 속성 지원 |
| IOS | 상단 숫자 키패드 + 하단 기호 키패드 (pattern="[0-9*]"을 사용하면 숫자 키패드만 보임) | _, +, # 부호를 포함한 숫자 키패드 |
| Android | 숫자 키패드 | _, +, # 부호를 포함한 숫자 키패드 |

전화번호는 input type="tel" pattern="[0-9]*"를 사용해서 숫자만 입력 받을 수 있도록 하고, 
이외의 숫자 키패드가 필요한 (가격, 우편번호, 신용카드. 보안코드. 나이, 시간 등)은 input type="number" pattern="[0-9*]"을 사용하여 IOS에서는 숫자 키패드만 보일 수 있도록 처리하는 것이 좋을 것 같다. (maxlength는 js로 처리한다는 전제하에!) 
pattern속성이 키패드도 제어하는 것인지, 받는 값을 제어하는 것인지 더 찾아봐야겟다. 

* 번외 : Ipad는 모두 숫자 + 하단 기호 키패드가 보임 (다만, 전화번호를 사용자가 저장해 두었다면 전화번호만 표시됨) 
 
### 2) CHECK BOX
* 단일서식때 label 미사용후 디자인 서식 사용
* 모든 디자인 요소 그려서 사용
* 레이블 내용이 두 줄 일 경우 대응
* IE 하위에서는 기본 UI로 노출
* 레이블까지 초점 잡히게
* js 사용하지 말고 checked사용
### 3) RADIO BUTTON
* 단일서식때 label 미사용후 디자인 서식 사용
* 모든 디자인 요소 그려서 사용
* 레이블 내용이 두 줄 일 경우 대응
* IE 하위에서는 기본 UI로 노출
* 레이블까지 초점 잡히게
* js 사용하지 말고 checked사용
* SEGEMENT BOX TYPE 화면이 작을 경우 떨어지는 문제 해결하기
* 별점 평가 TYPE css '~' 사용하는 법 알아보기
### 4) SELECT BOX
* drop_select (ssg 결제하기 참고)
### 5) FILE UPLOAD
* 추가되는 파일 명 보이게 개선
