.. |br| raw:: html

  <br/>

===================================================================
단일값 추가하기
===================================================================

| [단일값] 컴포넌트는 데이터의 내용, 기간 또는 타 컴포넌트와의 상호작용에 따라 변경되어 표시되어야 하는 대표값 중 단일 값의 형태를 띠는 데이터가 있을 때 쓰는 컴포넌트입니다.
| 예를 들어, 기간 내 발생한 로그 데이터의 총 수, 특정 고객의 수신 메일 개수와 같이 단일한 값만으로 통계적 의미를 가질 때 쓸 수 있는 컴포넌트입니다.

-------------------------------------------------------------------
사용 데이터
-------------------------------------------------------------------

본 튜토리얼에서는 약 5일치 미국 야구 타자들의 실적 데이터를 활용하였습니다.

.. image:: ./images/ko/single_value_01.png
    :alt: 미국 야구 타자들의 실적 데이터


-------------------------------------------------------------------
단일값 추가하기
-------------------------------------------------------------------

보고서 편집 화면에서 단일값 추가를 진행하겠습니다.


차트 영역 생성
=================================================================

.. image:: ./images/ko/single_value_02.png
    :alt: 단일값_차트영역생성

좌측 상단의 [차트] 버튼을 클릭한 후, 마우스 드래그&드롭하여 단일값을 추가하고자 하는 영역에 원하는 크기의 차트 영역을 생성합니다.


데이터 설정
=================================================================

.. image:: ./images/ko/single_value_03.png
    :alt: 단일값_데이터설정


| [단일값] 컴포넌트로 표시할 데이터는 결과값이 1개여야 합니다.
| 그래서 "stats" Command를 이용하여, 전체 선수의 홈런(H) 값의 평균을 표시하였습니다.
이를 위한 [검색어] 란에 아래와 같은 Command를 입력합니다.

.. code::

    데이터 Command: * | stats avg(H)


시각화 옵션 설정
=================================================================

.. image:: ./images/ko/single_value_04.png
    :alt: 단일값_시각화 옵션 설정

| 데이터 설정이 끝나면 우측 "시각화" 탭으로 이동합니다.
| "시각화 유형"에서 "단일값"을 선택한 후 하단의 "일반" 옆의 "시각화 옵션"을 클릭하십시오.

.. |opt1| image:: ./images/ko/single_value_05.png
    :alt: 단일값 시각화 옵션 (1)

.. |opt2| image:: ./images/ko/single_value_06.png
    :alt: 단일값 시각화 옵션 (2)

.. list-table::
   :header-rows: 1

   * - 옵션
     - 설명
   * - |opt1|
     - 단일값 글자의 글꼴, 색상, 크기, 스타일 등을 설정
       |br|
       |br| 다운로드 버튼과 상세보기 버튼 표시를 설정
   * - |opt2|
     - 가로/세로 정렬과 텍스트 정렬 방향을 설정

원하는 설정에 맞게 위 옵션들을 수정합니다.


결과 확인
=================================================================

설정을 마친 후 우측 하단의 [실행] 버튼을 클릭하면, 아래 그림과 같이 결과가 표시됩니다.

.. image:: ./images/ko/single_value_07.png
    :alt: 단일값 시각화 결과 확인


제대로 적용됐는지 확인하고자 한다면, 우측 상단의 [보기] 버튼 (주황색 상자로 표시)을 눌러 작성 결과를 다시 한 번 확인합니다.

.. image:: ./images/ko/single_value_08.png
    :alt: 단일값 시각화 결과 [보기]에서 확인

결과가 정상적으로 표출될 경우, 작성 화면에서 [저장] 버튼을 눌러 결과를 저장합니다.


-------------------------------------------------------------------
주의사항
-------------------------------------------------------------------

.. code::

    [Notice 01] [보기] 버튼을 눌렀을 때, 차트가 자동으로 실행되지 않을 경우

    차트의 경우, "자동 실행"을 설정하지 않을 경우 보고서 조회 시 자동으로 실행되지 않습니다.

    [데이터] 탭 하단의 [데이터 실행방법 설정]에 있는 "자동 실행"을 선택한 후 다시 확인해보시기 바랍니다.
    (아래 그림 참조)

.. image:: ./images/ko/autoplay.png
    :alt: 자동실행 설정


