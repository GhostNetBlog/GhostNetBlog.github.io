---
layout: post
title:  "GhostNet 초기 Architecture"
date:   2022-09-23 08:44:00 +0900
image:  /assets/images/blog/ghostnet_structure.drawio.png
author: Ghost
---

**GhostNet App은 Xamarin 기반으로 개발되었으나 Core는 분리되어 있다. 위 그림은 GhostNet의 Architecture를 보여준다. Layer 구조를 채택하였으며 철저히 단방향 의존성을 기준으로 구현되었다.**  

여러 Platform과 Server, Client을 분리 개발하기에는 시간이 많지 않았고 사용자의 Network환경에 따라 Master 노드가 될 수 있는 여부가 달라졌기 때문에 하나의 App에 Server와 Client를 모두 담아서 Release하였다.  

그렇지만 Server와 Client 모듈의 의존성을 분리하여 설계하였고 향후 3rd Party 앱을 지원하기 위해 Client 모듈을 분리가 잘 될 수 있도록 설계하였다.  

그 덕분에 Nuget Package로 Client Api를 분리하는 작업을 진행할 때 쉽게 할 수 있었다. 현재는 GhostOpenApi라는 이름으로 Nuget 사이트에 업로드 되어 있으며 Unity앱을 개발하면서 사용성을 개선하고 있다.  


#### Xamarin + UI Layer
Xamarin의 개발 프로젝트 구조를 보면 Core의 공용 프로젝트가 있고 각 Platform의 Native Code를 작성할 수 있는 프로젝트로 나뉘어저 있다. 여기서 최대한 신경쓴 점은 UI가 각 Platform에 독립적으로 설계되고 동일한 UI를 보여줄 수 있도록 한 점이다. PoC 버전이더라도 향후에 플랫폼이 확장할 경우를 생각하여 분리가 가능하도록 설계할 필요가 있었다.  

물론, Native Code를 사용할 수 밖에 없는 부분이 존재한다. Alram이라든지 image processing은 각 Platform이 지원하는 인터페이스를 사용해야한다. 

> 이번 App을 개발하면서 무엇보다도 중요한 것은 다양한 Platform에서 동작하는 App을 제작할 수 있는 역량을 확보한 점이다.

#### P2P Transport Layer
이 Layer는 네트워크를 담당하는 Layer이다. 단순히 TCP, UDP통신을 한다고 하면 socket api를 활용하면 문제가 없지만 이번에 구현할 기능은 `P2P` 기능이었다. 상당히 복잡하고 재미있는 기법들이 있어 흥미롭게 작업을 했다.  

보통 사용자 네트워크는 공유기와 같은 내부 네트워크로 묶여있는 경우가 많다. 내부 네트워크는 동적 IP 할당 방식을 사용하고 내부 네트워크에서만 유효한 IP를 갖는다. 대신 외부 네트워크에 연결될 때 공유기나 동적할당한 주체를 통해 port 매핑을 하여 연결되는데 이것을 NAT라고 한다. 두 개이상의 내부 네트워크의 동적 할당된 Ip들이 통신하기 위해서는 NAT를 통한 Hole Punch라는 기능을 구현해야한다.  

실제로 공유기의 특정 Port에 Packet을 전송해서 Hole를 뚫어 넣고 그 포트를 다른 네트워크에 존재하는 App으로 전송하니 Packet이 전달되었다. 시행착오도 많았는데 공유기에 따라 NAT를 유지하는 시간도 다르고 Port도 계속 변화하기 때문에 지속적으로 Heart Beat을 전송해야한다. 가상 사설망은 뚫지 못했는데 좀 더 네트워크를 공부해야겠다.  

#### Distributed & Clustering Network Layer

#### Block Chain Layer