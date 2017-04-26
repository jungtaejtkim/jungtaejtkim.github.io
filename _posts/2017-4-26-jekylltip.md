---
layout: post
title: 지킬(jekyll) 로 자신만의 github.io 블로그 만들기
category: Dev
tags: [blog, jekyll, github.io]
---

## 지킬 ??

지킬 ([Jekyll](http://jekyllrb.com)) 은 정적사이트나 블로그를 만드는 솔루션이다. 널리 알려져있는 워드프레스와 같다고 보면되는데, 차별화 되는 점은 워드프레스에 비해 블로깅과 정적사이트를 좀더 쉽게 만들고 가벼운 수준에서 쭉 운영해 나갈 수 있다는 점과, github 에서 pages 라는 서비스를 통해 무료로 호스팅을 해 나갈 수 있다는 점이 있겠다.

Jekyll 예시 사이트
1. [부트스트랩](https://react-bootstrap.github.io)
2. [페이스북 React](https://facebook.github.io/react/)


-----



## 지킬을 선택하게 된 배경

 그간 여러모로 블로깅을 해나가고싶었지만, 귀찮기도하고 늘 아직 일천하다는 생각이 있어 혼자 보는 로깅용 정도로만 하고 있었다.

 최근 기존 스타트업 전략이나 제품 기획외에 개발이나 제품디자인, 딥러닝 등 내가 커버해야하는 공부나 업무분야가 크게 확장되면서 자연스럽게 정보를 구해내는 소스도 다르게 되었는데, 이제는 대부분의 매체가 블로그, github, medium, youtube 등 특정 개인의 제작되어 오픈 어카이빙 되어있는 컨텐츠라는걸 깨닫게되고, 나도 하나 가져야겠다 싶어서 시작하게 되었다. 
 
 블로깅 툴로 여러가지를 고민했다. [Medium](http://www.medium.com),[Tumblr](www.tumblr.com),[Brunch](www.brunch.co.kr),[Tistory](www.tistory.co.kr),[Wordpress](www.wordpress.co.kr) 등을 고민하다가, 폐쇄적이고 몰입도도 높은 브런치로 결정하고 나의 이력을 작성하여 브런치 팀에 작가 신청을 하였다! 그리고 까였다!! 
 
 아무래도 기존 블로그나 컨텐츠, SNS 등 활동들을 한 로그가 필요했는데, 나는 거의 대부분이 사적인 로그였고 이거를 공개해서 재심사를 신청하기도 민망한 형태라서, 브런치를 가기위해 위 서비스 중 하나에서 블로깅을 하기로했다. 그렇다. 이 블로그는 브런치를 입성하기 위한 용도이다. 
 
 여러모로 검토하다가 웹 기반 블로그 서비스는 나에게 맞지않는다고 판단하였고 (비싸게 돈주고 산 키보드를 자주 쓰고싶었고), 워드프레스와 Jekyll 사이를 고민하다가 Jekyll 로 결정했다. 그 이유는 다음과 같다 
 
 * 텍스트기반의 블로깅 환경 - Jekyll 은 markdown 이나 html 로 글을 작성해야한다. 텍스트로만 작성해야하고, 이미지-비디오등 링크는 링크 태그 혹은 링크 마크다운을 통해 삽입해야만 하는 불편한 환경이다. 그런데 최근 나는 마우스를 사용하기보다는 대부분의 시간을 소스코드 편집에 쓰고 있었기 때문에, 이부분은 오히려 장점이었다
 
 * 지나치게 복잡해진 워드프레스 - 워드프레스는 이제 모르는 사람들이 없을 정도의 범용 도구이다. 사이트 저작용으로 쓰이기도하고 본디 목적인 블로깅용으로도 쓰이긴하지만, 제대로 블로깅을 위해 설치 해보고 여러가지 플러그인을 시험해본결과, 사이트 저작용 기능이 많아져서인지 몹시 무거워졌음을 확인 할 수 있었다. 그리고 워드프레스 환경에서 단축키도 많지않다는 점 때문에, 내게는 무겁고 - 복잡해 보이는 설치형 솔루션 이었다
 
 * github 과의 연동 - github 이 정식으로 지원하고, 무료로 호스팅을 제공한다는 매력이 있다. 그간 텀블러나 티스토리에 개인용 로그는 [내 개인 도메인](www.iamjtkim.com) 을 연결해 쓰고있었는데, 워드프레스 설치를 위해 알아본 대부분 서비스는 작게는 월 500원부터 5000 원까지 유료였다. 소액이지만 고정적인 지출처를 늘리기가 번거로웠고, 나는 이미 github 유료 유저였으며, 최근 가장 자주 방문하는 사이트가 github 이었기 때문에 그냥 '무료' 보다도 '관리의 이점' 이라는 측면에서 매력적이었다.

 * github.io - 사실 이 도메인의 간지가 jekyll 을 선택한 이유중 50% 는 차지했다고 봐도 무방하다. github pages 를 통해 jekyll 을 활성화 할 경우 github 은 username.github.io 형태의 url 을 무상으로 만들어준다. 그런데 이제 github.io 는 '나 tech 좀 알고 이걸로 밥도 좀 먹고 살아' 의 쿨한 상징과도 같아서 이에 이끌려 결정하였다. (워드프레스가 무료호스팅이며, 지킬수준으로 가볍고 텍스트 기반이라 할지라도 이것때문에 jekyll 을 선택했을 것이다 * ^^ * )


-----



## 지킬을 설치하기

지킬을 설치하는 방법은 두가지로 나뉜다. 

1. [github pages](http://pages.github.com) 에서 안내하는대로 거의 codeless 하게 설치하고 실행한다. 이 경우 github 환경설정에서 theme 등을 선택 할 수 있어서 대부분 블로그 서비스와 비슷하게 이용하면 되겠다

2. [github pages](http://pages.github.com) 에서 안내하는 초반 git clone 을 만든뒤에 jekyll 을 컴퓨터에 설치하여 local 하게 post 를 작성하고, git push 를 통해 업데이트 하는 방법


1번의 경우 [github pages tutorial](http://pages.github.com) 를 참고하여 그대로 진행하면되고, 여기서는 2번 방법을 설명한다.

/// 참고로 1번방법을 그대로 따라해서 jekyll 을 활성화 시키려면 튜토리얼내에 echo 명령어를 사용해서 만든 index.html 을 마지막에 꼭 지워줘야한다. 설정을 이리저리 바꿔도 Hello world 만 보고싶지않다면...

codeless 한 환경은 사용은 쉽지만 위에 말한 장점을 충분히 살리기 어렵기때문에 처음에 다소 어려워도 컴퓨터에 설치하도록 한다. 나는 맥 환경에서 설치를 진행하였다. 설치는 간단하지만 jekyll 은 ruby gem 환경이므로, 명령어 하나하나를 이해하려면 ruby 를 어느정도 알아야한다. 초기 설치시에만 ruby 관련 명령어를 쓰고 완료된 뒤엔 ruby 쳐다볼일 없으니 그냥 그대로 따라 치는게 편하다.

1. www.github.com 에서 계정을 만든다

2. 계정을 만든뒤 "create repository" 클릭

3. repository name 을 깃헙계정이름.github.io, 만약 계정이름이 jtkim 이라면 jtkim.github.io 를 입력한다

4. public 과 private 을 설정하면되는데, 이는 github 이나 googling 을 통한 공개여부를 결정한다. 오픈소스 / 배타적소스 라고 보면 될 것 같다. private 으로 설정하려면 월단위 과금을 선택하거나, 학생 특전을 받으면된다. 그런데 공개 블로그에는 그렇게 까지 보호할 만한 자료는 없을것이므로 그냥 public 으로 해도 무방하다.

5. init readme.md 를 체크한뒤 repository 를 만든다

6. 그 뒤 초기 git 설정 메시지가 나오는데, 익숙하거나 해당 메시지에 익숙하신분들은 그대로 설정하면 되고, 아니면 아래 메시지를 따르면 된다

7. 터미널을 실행한다

8. desktop 이나 document 같은 접근하기 편한 경로로 이동한다. {% highlight js %} 
cd desktop
// or 
cd document
{% endhighlight %} 

9- 다음 코드를 기입한다 {% highlight js %} 
git clone "https://깃헙유저네임.github.io"
{% endhighlight %}

10- 만들어진 clone 폴더에 들어가서, git 을 처음으로 연결(init) 하고 제출(commit) 한다. {% highlight js %} 
cd 깃헙유저네임.github.io  
// 해당 폴더로 진입 
git add -all
// git init
git commit -m "첫번째로 코드와함께 제출할 메모"
// git commit
git push -u origin master  
// 이 이후부터는 git push 명령어만 입력하면된다
{% endhighlight %}

11- 이제부터 컴퓨터에 github 과 연동되는 jekyll 을 설치하는 작업이다. 현재까지 있던 github.io 에서 벗어난뒤 루비 버전을 확인 후 지킬을 설치한다.
{% highlight js %}
cd ..
// 해당 폴더를 벗어난다
ruby -v
// ruby 버전을 확인한다. 2.3 점대 버전 이상이면 된다. 대부분의 맥환경에서는 걱정할일 없다 
sudo gem install jekyll
// 지킬 gem 을 깐다
jekyll new 아무폴더이름
// 지킬이 적용된 파일 폴더를 만든다 
jekyll serve --watch 
// 명령어 입력후 사파리나 크롬을 연뒤 [http://localhost:4000](http://localhost:4000) 으로 가보면 jekyll 이 컴퓨터에서 돌고있음을 확인 할 수 있다. 
{% endhighlight %}
12- 지금 만든 폴더의 내용물을 빠짐없이 아까 git 을 clone 한 폴더로 복사한다. 빠짐없이 복사하기위해선 맥의 command + shift + > 를 누르면 숨김파일까지 나오는데, 해당 파일까지 이동시키면 된다. 터미널을 이용하지 않아도된다.
13- 다시 터미널을 통해 github.io 폴더로 이동한뒤에 이제 jekyll 을 git 에 올려준다 
{% highlight js %}
cd username.github.io
git add * 
//git add -all 과 같은 명령어
git commit -m "install jekyll"
git push
{% endhighlight %}

14- 1분 정도 기다린뒤 자신의 username.github.io 를 주소창에 입력한다. 정상 접속 되면 그대로 마무리이다.



## 지킬 꾸미기
 지킬은 html 과 css, scss 등 customization 을 지원하지만 그렇게 해서 꾸밀거면 사실 처음부터 새로 만들고 말지.... 아래 방식을 통해 꾸미도록 해보자.
 
 
 나는 아래 테마를 사용하였다 
* 테마 데모 사이트 - [https://codinfox.github.io](https://codinfox.github.io)
* 테마 git - [https://github.com/codinfox/codinfox-lanyon](https://github.com/codinfox/codinfox-lanyon)



1. jekyll 로 운영중인 타인의 github.io 사이트를 찾는다. "tech blog github.io" 나 "design blog github.io" 로 검색해서 여러개를 방문해거나 이미지 검색해서 자신이 원하는 디자인과 기능을 갖춘 테마를 찾는다. 

2. 그런 github.io 의 블로그들은 자신이 쓰는 테마를 자신의 git 에 opensource 로 공유해둔다. github.io 의 메뉴중에 직접 자신의 git 으로 대부분 링크를 걸어두었으니 그곳으로 이동한다. 

3. 해당 git 으로 이동한뒤 우측 상단 Star, Folk... 등등에서 folk 를 누르고 자신의 계정으로 해당 jekyll theme 를 복사해온다. 매너인 star 누르기를 잊지 말자. 

4. 복사된 자신의 계정 내 theme git 으로 가서 우측 상단에 초록색으로 빛나는 "Clone or download" 를 클릭하여 다운로드 받는다. 

5. 자신의 username.github.io 컴퓨터 폴더로 이동하여 gemfile, gemfile.lock 를 제외하고 전부 다른곳으로 이동시킨다 (삭제하지말고 혹시모르니 백업하라는 의미).  간혹 gitignore 라는 파일때문에 아래 절차가 진행이 안될수 있다. 이 경우 깔끔하게 이동시키려면 역시 command + shift + > 를 활용.

6. 다운로드 받은 테마파일을 내 username.github.io 로 복사한다

7. 제대로 복사되었는지 확인한다
{% highlight js %}
cd username.github.io
// 해당 폴더로 이동
jekyll serve --watch
// 명령어 실행 후 사파리, 크롬을 통해 localhost:4000 으로 이동해서 확인
{% endhighlight %}
8. 터미널을 실행시킨후 커밋, 푸쉬한다 
{% highlight js %}
cd username.github.io
// 해당 폴더로 이동
git add *
// 변경사항 add
git commit -m "copy theme"
// 남기고 싶은 해당 버전의 commit 에 대한 메모를 기입
git push
{% endhighlight %}

9- username.github.io 사이트에 방문하여 제대로 적용 되었는지 확인한다. 더미 컨텐츠와 튜토리얼을 통해 테마 제작자가 남긴 주의사항을 염두에 두고 향 후 블로깅을 하면 된다

10- 컴퓨터 내 github.io 폴더에서 _config.yml 을 연다. 거기서 자신의 이름, 컨택트등 정보를 기입해준다. 기입이 완료되면 git push

11- jekyll github io blog 완성


 
 이렇게 해서 설치가 완료되었다. 다음은 jekyll 과 markdown 을 이용한 라이팅 방법을 포스팅 해보도록 하겠다.
 
 
 
 