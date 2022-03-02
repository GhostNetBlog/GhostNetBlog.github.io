---
layout: page
title: 블록체인 
permalink: /blockChain/
---

<h1 class="page-title">{{ page.title | escape }}</h1>

<div class="container">
      <div class="row">      
          <div class="col s12 m4 l6 center">     <br><br>
            <img width="400" data-action="zoom" src='{{ "/assets/imgs/masternetwork.png" | relative_url }}' alt='absolute'> 
          </div>
          <div class="col s12 m4 l6 left">    
          <h5> 개요</h5>
          GhostNet에서 블록체인은 크게 마스터 노드와 일반 노드로 구분됩니다. <br>
          마스터 노드는 Ghost Net을 구현하는 블록체인 네트워크를 구성하는 중요한 노드입니다. <br><br>
          Ghost Net에서는 중앙서버가 없기 때문에 마스터 노드들이 Peer-to-Peer 방식으로 네트워크를 관리하고 그에 대한 보상으로 코인을 받습니다. <br><br>
          일반 노드는 마스터 노드가 제공하는 서비스를 기반으로 SNS, 메신져, NFT 거래 등을 이용할 수 있습니다. <br><br>
          <h5>마스터 노드 자격</h5>
          마스터 노드는 일반 노드가 언제든지 접속 가능해야하기 때문에 아이피 주소가 변동되면 안됩니다. <br> <br>
          따라서 PC 버전의 앱만 마스터 노드가 될 수 있는 자격이 되며 PC 버전에서도 네트워크 환경에 따라 마스터 노드가 될 수 없는 경우가 존재합니다.<br><br>
          마스터 노드가 될 수 없는 경우는 가상 네트워크 환경(사설망, VPN, 공유기등)에 있는 경우 입니다. 이 경우 외부에서 접근할 수 없기 때문에 마스터 노드가 될 수 없습니다.<br><br>          
          </div>
      </div>
      <div class="row">    
          <div class="col s12 m4 l6 left">    
          <h5>마스터 노드의 채굴</h5>
          GhostNet은 다른 블록체인과 달리 해시 계산을 통해 채굴을 하지 않습니다. 해시 파워에 의존하지 않고 팔로우, 팔로워 관계를 기반으로 채굴을 수행합니다. <br><br>
          일반 노드가 NFT나 코인을 다른 사람에게 송금할 경우 연결된 마스터가 거래를 중계하고 관리합니다. <br>
          그리고 트랜잭션마다 마스터의 주소가 기록되며 모든 마스터에게 공유됩니다.<br><br>
          그리고 일정 트랜잭션을 수집한 마스터는 블록을 생성할 수 있으나 블록 생성하는 행위만으로 보상을 받지 않습니다.<br><br>
          블록이 생성될 때 해당 블록을 구성하는 트랜잭션들을 기존으로 보상이 분배됩니다.<br><br>
          각 트랜잭션마다 거래를 중계한 마스터들이 기록되어 있으며 블록을 구성하는 트랜잭션 비율로 나누어 코인을 갖습니다.<br><br>
          예를 들어 하나의 블록에 마스터 A 의 트랜잭션 2개, 마스터 B의 트랜잭션 3개로 구성되어 있으면 2:3의 비율로 보상을 받습니다.<br><br>
          마스터 노드는 팔로워가 많을 수록 더 많은 보상을 받을 확률이 높아집니다.
          </div>  
          <div class="col s12 m4 l6 center">     
            <img width="400" data-action="zoom" src='{{ "/assets/imgs/masternetwork2.png" | relative_url }}' alt='absolute'> 
          </div>
      </div>
      <div class="row">      
          <div class="col s12 m4 l6 center">     <br><br>
            <img width="400" data-action="zoom" src='{{ "/assets/imgs/masternetwork3.png" | relative_url }}' alt='absolute'> 
          </div>
          <div class="col s12 m4 l6 left">           
          <h5>마스터 프랜즈</h5>
          마스터 노드만 채굴에 참여할 수 있기 때문에 일반 노드는 채굴의 기회를 갖기가 어렵습니다. 
          반대로 팔로워가 많은 일반 노드가 존재 할 수 있습니다.<br><br> 
          팔로워가 많은 일반 노드느 마스터 노드와 합의하여 마스터 프랜즈가 될 수 있습니다.
          마스터 프랜드의 팔로워는 마스터 프랜드와 함께 마스터 노드 사용하며 마스터 노드와 프랜드는 보상을 나누어 갖습니다.<br><br>      
          <h5>블록 생성 규칙</h5>
          블록은 10초를 기준으로 생성될 수 있게 난이도가 조절되도록 설계되어 있습니다. 다른 블록체인은 해시 파워를 통해 난이도를 조절하지만 GhostNet은 Transaction의 숫자로 난이도를 조절합니다. 예를들면 한 시간동안 생성된 블록의 트랜잭션수를 보고 다음 한시간의 블록에 최소 트랜잭션 갯수를 정합니다. <br><br>
          하나의 블록에 포함되는 트랜잭션에는 동일한 마스터의 트랜잭션 수를 제한합니다만 테스트 기간 동안에는 약한 제한만이 있습니다.     
          <br><br> <br><br>    
          </div>
      </div>
</div>