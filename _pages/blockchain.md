---
layout: page
title: BlockChain
---

<section class="section">
  <div class="container">
    <div class="row justify-content-around">    
      <div class="col hover-shadow pt-3">
        <br>
        <h3> 개요</h3>
        GhostNet에서 블록체인은 크게 마스터 노드와 일반 노드로 구분됩니다. 마스터 노드는 Ghost Net을 구현하는 블록체인 네트워크를 구성하는 중요한 노드입니다. Ghost Net에서는 중앙서버가 없기 때문에 마스터 노드들이 Peer-to-Peer 방식으로 네트워크를 관리하고 그에 대한 보상으로 코인을 받습니다. 일반 노드는 마스터 노드가 제공하는 서비스를 기반으로 SNS, 메신져, NFT 거래 등을 이용할 수 있습니다.  
        <br>
        <img width="400" data-action="zoom" src='{{ "/assets/imgs/masternetwork.png" | relative_url }}' style="display:block;width:40%;margin:0px auto">  <br><br>
        <br>
        <li>Grand Master Node</li>
        <li>Master Node</li>
        <li>Master Friend Node</li>
        <li>Normal Node  </li>
      </div>
    </div>
    <div class="row">
      <div class="col hover-shadow pt-3">
        <h3>마스터 노드 자격</h3>
        마스터 노드는 일반 노드가 언제든지 접속 가능해야하기 때문에 아이피 주소가 변동되면 안됩니다. 따라서 PC 버전의 앱만 마스터 노드가 될 수 있는 자격이 되며 PC 버전에서도 네트워크 환경에 따라 마스터 노드가 될 수 없는 경우가 존재합니다. 
        마스터 노드가 될 수 없는 경우는 가상 네트워크 환경(사설망, VPN, 공유기등)에 있는 경우 입니다. 이 경우 외부에서 접근할 수 없기 때문에 마스터 노드가 될 수 없습니다. <br>
        <img width="400" data-action="zoom" src='{{ "/assets/imgs/masternetwork2.png" | relative_url }}' alt='absolute' style="display:block;width:40%;margin:0px auto">
      </div>
    </div>
    <div class="row">    
      <div class="col hover-shadow pt-3">
        <h3> 마스터 노드의 채굴</h3>
        GhostNet은 다른 블록체인과 달리 해시 계산을 통해 채굴을 하지 않습니다. 해시 파워에 의존하지 않고 특별한 알고리즘을 사용하여 팔로우, 팔로워 관계를 기반으로 채굴을 수행합니다.  
        따라서 마스터 노드는 팔로워가 많을 수록 더 많은 보상을 받을 확률이 높아집니다.<br>
        <img width="400" data-action="zoom" src='{{ "/assets/imgs/masternetwork3.png" | relative_url }}' alt='absolute' style="display:block;width:40%;margin:0px auto"> 
      </div>
    </div>
    <div class="row">
      <div class="col hover-shadow pt-3">
        <h3>마스터 프랜즈</h3>
        마스터 노드만 채굴에 참여할 수 있기 때문에 일반 노드는 채굴의 기회를 갖기가 어렵습니다. 
        반대로 팔로워가 많은 일반 노드가 존재 할 수 있습니다.  
        팔로워가 많은 일반 노드느 마스터 노드를 활용하여 마스터 프랜즈가 될 수 있습니다.
        마스터 프랜드의 팔로워는 마스터 프랜드와 함께 마스터 노드 사용하며 마스터 노드와 프랜드는 보상을 나누어 갖습니다.  
      </div>
    </div>
    <div class="row">
      <div class="col hover-shadow pt-3">
        <h3>블록 생성 규칙</h3>
        블록은 `1분`을 기준으로 생성될 수 있게 난이도가 조절되도록 설계되어 있습니다. 다른 블록체인은 해시 파워를 통해 난이도를 조절하지만 GhostNet은 Transaction의 숫자로 난이도를 조절합니다. 예를들면 한 시간동안 생성된 블록의 트랜잭션수를 보고 다음 한시간의 블록에 최소 트랜잭션 갯수를 정합니다.
        하나의 블록에 포함되는 트랜잭션에는 동일한 마스터의 트랜잭션 수를 제한합니다만 테스트 기간 동안에는 약한 제한만이 있습니다.  
      </div>
    </div>
  </div>
</section>