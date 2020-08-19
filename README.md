# responsive_web_practice

## 왜 float를 사용할 때 overflow: hidden을 사용하나?

출처 : https://simssons.tistory.com/26

그렇다면 overflow가 뭔데 자동으로 float 잡아주나?

width, height 특징
width auto : 부모만큼
height auto: 컨텐츠만큼

1. height:auto;는 자신이 포함한 컨텐츠의 높이값을 자신의 높이값으로 하는것.


    그러나 안의 자식 left_box가 float이 되면 그 부모인 wrap은 컨텐츠를 잡지 않는 것이 되어서 한줄로 줆.

2. 이때 overflow:hidden;을 주면 해결이 된다. 왜?


    overflow:hidden;은 **주어진 사이즈**만큼만 보여줌. 자신에게 주어진 사이즈만 나타내고,

    자신의 크기를 넘어서는 것(overflow)은 숨긴다(hidden)!

3. 따라서, wrap에 overflow: hidden을 주면, wrap은 주어진 사이즈만큼의 height을 가지고


    이를 넘어가는 것을 숨긴다. 그렇다면 wrap에게 주어진 높이는?  wrap의 height:auto;니까

    wrap이 포함하는 컨텐츠 높이가 자신의 높이가 됨. 즉, left_box의 높이가 자신의높이가 됨.

    그래서 float으로 뜬 컨텐츠도 깨지지 않고 원하는대로 보이게 하는 것임.
