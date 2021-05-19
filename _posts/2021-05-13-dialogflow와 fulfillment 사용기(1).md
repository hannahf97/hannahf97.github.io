___

layout: post
title:  "dialogflow와 fulfillment 사용기 (1)"

---

**#01 dialogflow 와 fulfillment 사용 **

-------------------------------

졸업 프로젝트로 현재 dialogflow를 이용해 주문 제작 챗봇을 개발하고 있다

그러던 와중 dialogflow에 말이 매끄럽게 이어지지 않은 부분이 있어서 고민중이다.



현재 생각으로는

"" 기기 "" -> ""이용자 ""  에게 햄버거, 음료, 사이드 메뉴 중 하나를 선택하라

""" 이용자""" -> ""기기"" 에게 햄버거 ! 를 외치면

"" 기기 "" -> ""이용자 ""  에게 햄버거를 선택하셨습니다 햄버거에는 이쁜이버거, ~라는 리스트를 말하고 

버거 설명 / 버거 주문 / 다른 메뉴 주문 을 선택하는 형태로 넘어가게 만들고 싶다



```JSON
<pre>
<code>
 function selectmenu(agent){
    const burger = agent.parameters.Burger;
    const side = agent.parameters.Side;
    const drink = agent.parameters.Drink;
    if (burger){
      agent.add("${burger}에는 이쁜이버거,게살버거, 치즈버거가 있습니다. 셋중 하나를 선택해주세요");
                }
    else if (side){
        agent.add("${side}에는 부리또, 샐러드가 있습니다. 둘중에 하나를 선택해주세요");
    }
    else if(drink){
      agent.add("${drink}에는 콜라 사이다가 있습니다. 둘중 하나 선택해주세요");
    }
  }
</code>
</pre>
```



라고 써봤는데 일단 되지 않는다

그나저나 구글 무료 평가판,,,>?

나 33만원 내야하는거 아니지,...?

 ㅜㅜㅜㅜㅜㅜ



