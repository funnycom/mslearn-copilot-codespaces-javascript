[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526682619)

# 깃허브 코파일럿을 사용해 자바스크립트 작성하기

깃허브 코파일럿을 사용해 자바스크립트 저장소를 어떻게 수정하는지 알아봅시다. 깃허브 코파일럿은 웹 애플리케이션을 수정하거나 커스터마이징하는 코드를 제안해 줍니다. 
자바스크립트 저장소를 통해 빠르고 간편하게 포트폴리오 사이트용 자바스크립트 웹 앱을 만들 수 있습니다. 

## 필수 조건

1. [깃허브 코파일럿 서비스](https://github.com/github-copilot/signup)를 사용할 수 있어야 합니다. 
1. [코드 스페이스에 저장소(repository)가 있어야 합니다](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-javascript?quickstart=1)

## 💪🏽 직접 해 보기

여기에서 제공하는 템플릿 포트폴리오는 리액트(React) 기반의 웹 애플리케이션으로, 웹 브라우저를 통해 손쉽게 커스터마이징하고 배포할 수 있도록 준비했습니다. 
In this template portfolio, we have a React based web application ready for you to easily customize and deploy using only your web browser.


### 🛠 1 단계 : 웹 앱 커스터마이징하기

자신에게 맞게 포트폴리오를 커스터마이징해 보겠습니다. 
src/App.jsx 파일을 열어 siteProps를 수정하세요. siteProps 변수는 사이트 커스터마이징에 필요한 값들을 '키:값' 형태로 포함하는 자바스크립트 객체입니다.
아래와 같이 생겼죠.

```javascript
const siteProps = {
  name: "Alexandrie Grenier",
  title: "Web Designer & Content Creator",
  email: "alex@example.com",
  gitHub: "microsoft",
  instagram: "microsoft",
  linkedIn: "satyanadella",
  medium: "",
  twitter: "microsoft",
  youTube: "Code",
};
```

### 🔎 2단계 : 프롬프트를 통해 소셜 미디어 아이콘 애니메이트하기

이어서 주석을 추가하는 형태로 깃허브 코파일럿을 사용해 새로운 엔드포인트를 만들어 보겠습니다.

애니메이션을 사용하면 소셜 미디어 섹션을 더욱 눈에 띄게 할 수 있겠죠? 아이콘을 움직이도록 하기 위해 코파일럿에게 도움을 요청해 보겠습니다.
src/style.css 파일에 아래 코드처럼 코멘트 형식의 프롬프트를 추가하세요.

```css
/* add an amazing animation to the social icons */
```

The suggestion from Copilot should look similar to the following:

```css
img.socialIcon:hover {
  animation: bounce 0.5s;
  animation-iteration-count: infinite;
}

@keyframes bounce {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
```

### 🚀 Step 3: Work with the suggestion

Accept the suggestion by pressing the tab key. If you don't receive the exact same suggestion, then you can either experiment with the suggestion provided or keep typing the CSS code until it matches.

Your site should already be running in your Codespace, and the change will reload onto the page automatically. To see them, hover over one of your social media icons in the footer to see the magic!


Congratulations, through the exercise, you haven't only used copilot to generate code but also done it in an interactive and fun way! You can use GitHub Copilot to not only generate code, but write documentation, test your applications and more.
