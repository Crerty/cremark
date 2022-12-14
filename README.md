<img src="https://user-images.githubusercontent.com/65072459/183138115-56b752fa-13a1-4d1f-82e0-0fcc5b88f6c6.png" width="150">
cremark는 나무마크의 문법을 일부 개선하고 다양한 기능을 추가한 문법입니다.

-----

나무마크 문법이 다른 마크업 언어에 비해 깔끔한 건 사실이나, 여러 문제점이 존재합니다. cremark는 이러한 문제점을 해결하고, wiki style 등을 통해 비공식적으로 구현한 문법을 공식적으로 도입하며, 이용자가 더욱 편하게 사용할 수 있도록 나무마크를 개선한 결과입니다.

대부분의 문법은 두 개의 기호로 시작과 끝을 구분합니다. (ex *\*굵게\*\*, [[동영상:파일]])

매개변수 입력란은 |로 구분하며, 쉼표를 붙여 구분합니다. 또한 값 입력형과 단독형이 있습니다. **멀티미디어에서 단독형 매개변수 사용 시 반드시 앞에 #를 붙여 구분해야 합니다.**

상위 문서 이동은, 시스템상 한계로 예외가 너무 많아 삭제합니다. 직접 링크해야 합니다.

리다이렉트 기능은 개발 중인 엔진에서 지원할 예정이며, 직접 입력하는 리다이렉트는 사라질 예정.

단계를 구분하는 문법은 1~6 단계로 나눕니다.

```
**굵게**
//기울임//
__밑줄__
~~취소선~~
''위첨자''
,,아래첨자,,
{{리터럴}}
\문법미적용 ex [\[링크]] > [[링크]]

{{텍스트|textcolor=#color, #color}}
{{텍스트|+3, textcolor=#color,#color, bgcolor=#color, #color}}
** bgcolor 미사용시 textcolor= 생략 가능**
ex) {{텍스트|#color, color}}

컬러 두개 쓸 땐 붙여쓰기
#color, +1, #color 안됨
#color, #color, +3 가능

---

[[링크]]
[[문서:문서]]
[[사용자:사용자문서!]]
[[링크|출력]]
[[링크|{{텍스트|#color}}]]
[[링크=기능|문단]]
[[링크=6.2|문단]]
[[/하위]]

[[https://crerty.com]]
[[https://crerty.com|아웃링크]] 

[[이미지:파일.png]]
[[이미지:파일.png]]
[[이미지:파일.png|width=1, height=3, align=right]]
[[이미지:파일.jpg|height=3, #center, width=5]]

[[동영상:파일명.mp4|width=1, align=center]]
[[동영상:link.com|매개변수=1]]
동영상은 링크 걍 집어넣으면 알아서 변환하나, 유명한 사이트의 링크만 허용(보안)

[[이미지:파일.png|단순링크]]
[[동영상:동영상.mp4|]] 출력결과 : 동영상:동영상.mp4

[[분류:분류|#blur]]
[[틀:창틀|매=1,개=2,변수=3]]

역시 단순 링크시에는 끝에 | 붙이며, 이름이 매개변수와 충돌시 \ 적절히 사용
사용자 문서나 일반문서 불러오는 인클루드 일단 미구현, 사용할데가 별로 없음.
혹은 [[사용자:test|#include]], 틀은 저 인클루드 생략하는 등의 방식 고민중. 다만 문법 파편화 우려

---

표
나무마크와 동일, 딱히손볼거--없음-- 있음. 주로 wiki style을 통해 복잡하게 구현한 일부 문법 표준화

매크로

= 문단
== 문단
=== 문단
==== 문단
===== 문단
====== 문단

= #문단
==#문단
=== #문단
==== #문단
===== #문단
====== #문단

 * list
  * 2nd list
    * 3rd list

 1. List!
   2. List

 A. List
 B. List

---

<<각주>>
<<각주인데 텍스트?|A>>

""인 용 문""
""인용문 방문 "" 의문 가슴이떨리는건너때문""숭례문""""

수평줄
한 줄에 완전 비었을 때
-부터 ------까지

---

매크로
((매크로이름|변수)) 형식

((date)) 또는 ((datetime))
((date|시간대))), ((datetime|시간대)) 등도 가능

((dday|YYYY-MM-DD))
((목차)) 또는 ((tableofcontents)) 또는 ((toc))
((각주)) 또는 ((footnote)) 또는 ((fn))

((br))
((clearfix))
