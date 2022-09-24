---
layout: post
title:  "GhostNet 초기 Architecture"
date:   2022-09-24 08:44:00 +0900
image:  /assets/images/blog/ghostnet_structure.drawio.png
author: Ghost
---

**GhostNet App은 Xamarin 기반으로 개발되었으나 Core는 분리되어 있다. 위 그림은 GhostNet의 Architecture를 보여준다. Layer 구조를 채택하였으며 철저히 단방향 의존성을 기준으로 구현되었다.**  

여러 Platform과 Server, Client을 분리 개발하기에는 시간이 많지 않았고 사용자의 Network환경에 따라 Master 노드가 될 수 있는 여부가 달라졌기 때문에 하나의 App에 Server와 Client를 모두 담아서 Release하였다.  

그렇지만 Server와 Client 모듈의 의존성을 분리하여 설계하였고 향후 3rd Party 앱을 지원하기 위해 Client 모듈을 분리가 잘 될 수 있도록 설계하였다.  

그 덕분에 Nuget Package로 Client Api를 분리하는 작업을 진행할 때 쉽게 할 수 있었다. 현재는 GhostOpenApi라는 이름으로 Nuget 사이트에 업로드 되어 있으며 Unity앱을 개발하면서 사용성을 개선하고 있다.  


#### Xamarin + UI Layer
Xamarin의 개발 프로젝트 구조를 보면 Core의 공용 프로젝트가 있고 각 Platform의 Native Code를 작성할 수 있는 프로젝트로 나뉘어저 있다. 여기서 최대한 신경쓴 점은 UI가 각 Platform에 독립적으로 설계되고 동일한 UI를 보여줄 수 있도록 한 점이다. PoC 버전이더라도 향후에 플랫폼이 확장할 경우를 생각하여 분리가 가능하도록 설계할 필요가 있었다.  

> 물론, Native Code를 사용할 수 밖에 없는 부분이 존재한다. Alram이라든지 image processing은 각 Platform이 지원하는 인터페이스를 사용해야한다. 