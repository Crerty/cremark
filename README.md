# Newmark
뉴마크

namumark와 호환되나, 비효율적인 문법을 일부 개선하고 기능을 추가한 문법입니다.
이름은 아마도 바뀔 겁니다.

Newmark

텍스트 / 멀티미디어 / 표 / 매크로 / 기타로 통합
예외를 최대한 줄입니다.
기타 문법을 제외한 나머지는 모두 두개로 시작합니다. (ex **굵게**, [[동영상:파일]])

비슷하거나 겹치는 문법은 없어야 합니다.
매개변수 입력란은 |로 구분하며, 쉼표를 붙여 구분합니다. 그 다음 내용은 쉼표를 붙이지 않고 띄어 써 구분합니다.

매개변수는 영어=값(px가 기본값이며 생략, %이나 기타 값 허용)으로 구분합니다. 다만 단순내용이나 단순 구분 용도일 때는 =값 생략 가능합니다. (ex: [[|width=1, right]] [[분류:분류|blur]]

#는 무언가를 숨기거나, 색상을 표현할 때 사용합니다.

상위 문서 이동은, 시스템상 한계로 예외가 너무 많아 삭제합니다. 직접 링크해야 합니다.

---

```Text

**굵게**
//기울임//
__밑줄__
~~취소선~~
^^위첨자^^
,,아래첨자,,
{{리터럴}}

{{+1~6 텍스트}}
{{-1~6 텍스트}}
{{#color 텍스트}}
{{#color, #color 텍스트}}
{{+1, #color 텍스트}}
{{+2, #color, #color 텍스트}}

Multimedia

[[링크]]
[[링크|출력]] [[링크|name=출력]]이 생략된 것.
[[링크|{{-3, #color 텍스트}}]]
[[링크=기능|문단]]
[[링크=6.2|문단]]
[[/하위]]

[[https://crerty.com]]
[[https://crerty.com|아웃링크]] 역시 name=아웃링크가 생략된 것.

[[이미지:파일.png]]
[[이미지:파일.png]]
[[이미지:파일.png|width=1, height=3, align=right]]

단순링크시 [[:이미지.png]]

[[동영상:파일명.mp4|width=1, align=center]]
[[동영상:link.com]]
.youtube
.nico
.vimro
.navervid
.fbvideo
최적화

[[분류:분류|blur]]

표

쓰는중

매크로

=문단
==문단
===문단
====문단
=====문단
======문단

=#문단
==#문단
===#문단
====#문단
=====#문단
======#문단

 * list
  * 2nd list
    * 3rd list

 1. List!
   2. List

 A. List
 B. List

<<:각주>>
<<:A 각주인데 텍스트?>>
<<:각주 <<:안 각주를 제한할 필요가 있어요?>>>>

>인 용 문
>> 인 용 문
>>> 인 용 문

수평줄은 ---만 허용,```
