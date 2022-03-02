---
layout: page
title: 시작하기
permalink: /start/
---

<h1 class="page-title">{{ page.title | escape }}</h1>

<div class="container">
      <div class="row">      
          <div class="col s12 m4 l6 center">     
            <img width="300" data-action="zoom" src='{{ "/assets/imgs/1_loginpage.png" | relative_url }}' alt='absolute'> 
          </div>
          <div class="col s12 m4 l6 left">    
          <h5> 시작하기</h5> 
          앱을 시작하면 다음과 같이 로그인 화면이 나타납니다. 로그인 화면에서는 다음과 같은 동작을 할 수 있습니다<br><br>
          <li>마스터 노드 선택하기</li>
          <li>로그인하기</li>
          <li>신규 계정 만들기</li>
          <li>계정 복구 하기</li><br><br>
          로그인과 계정 관련 동작을 할 경우 반드시 마스터 노드의 선택이 선행되어야 합니다.          <br><br>
          <h5>로그인 하기</h5>
          로그인시에는 기기에 저장된 계정리스트에서 선택하고 암호를 입력하면 됩니다. 공개키는 기억하거나 타이핑하기 어렵기 때문에 별명을 통해 공개키를 사용하도록 되어 있습니다. 
          마스터 노드에서 개인키와 서명이 인증되면 로그인을 허용합니다.
          </div>
      </div>
      <div class="row">      
          <div class="col s12 m4 l6 left">  
          <h5> 마스터 노드 선택</h5>
          마스터 노드는 블록체인 네트워크를 통해 이뤄지는 모든 동작을 중계하는 주체기 때문에 마스터 노드의 자체 성능이나 네트워크 상태에 따라 자신의 동작 성능에 영향을 받습니다. <br><br>
          때문에 마스터 노드 선택이 중요합니다. 마스터 노드는 네트워크를 탐색하여 조회할 수 있으며 특정 마스터 노드를 검색해 선택할 수 있습니다.
          마스터 노드를 기반으로 네트워크가 동기화되기 때문에 변경하지 않는 것이 더 효율적으로 동작 가능합니다.
          </div>
          <div class="col s12 m4 l6 center">   
            <img width="300" data-action="zoom" src='{{ "/assets/imgs/2_makeaccount.png" | relative_url }}' alt='absolute'> 
          </div>
      </div>
      <div class="row">      
          <div class="col s12 m4 l6 center">     
            <img width="200" data-action="zoom" src='{{ "/assets/imgs/2_makeaccount.png" | relative_url }}' alt='absolute'> 
            <img width="200" data-action="zoom" src='{{ "/assets/imgs/3_makeaccount.png" | relative_url }}' alt='absolute'> 
          </div>
          <div class="col s12 m4 l6 left">
          <h5> 신규 계정 만들기 </h5>
          블록체인 네트워크는 공개키와 개인키 쌍으로 계정이 관리됩니다. 개인키는 자신의 기기와 고스트넷에 암호화되어 저장됩니다. <br><br>
          고스트 넷은 개인키를 네트워크에 저장하는 기능을 제공하고 있는데 복구용 암호를 통해 암호화되어 저장됩니다. 복구 암호는 한번 정하면 변경할 수 없으므로 신중하게 결정해야하며 기억하고 있어야합니다. 고스트넷은 암호를 복구 할 수 있는 기능이 없습니다.
          <br><br>
          공개키는 자신을 특정할 수 있는 고유의 키이지만 기억하거나 관리하기 어렵기 때문에 고스트넷은 별명을 제공하고 있습니다. 별명은 개인키를 찾기위한 유용한 방법이지만 고스트넷 구조상 낮은 확률로 중복이 발생할 수 있습니다. 
          <br><br>
          신규 계정이 만들어지기 위해서 계정을 등록하는 트랜잭션이 블록에 포함되어 블록체인을 완성해야합니다. 경우에 따라서 계정을 만들고 바로 로그인이 되지 않을 수 있습니다.
          </div>
      </div>
      <div class="row">      
          <div class="col s12 m4 l6 left">   
          <h5>계정 복구 하기</h5>
          개인키는 자신의 기기와 고스트넷에 저장됩니다. 평소에는 자신의 기기에 저장된 개인키를 사용하지만 기기를 변경할 경우 개인키를 잃어버리게 됩니다. 
          <br><br>새로운 기기에서 로그인을 하기 위해서는 계정을 복구해야합니다. 신규 계정을 만들때 입력한 복구용 비밀번호를 통해 개인키를 다운받아 저장합니다. 이때 새로운 비밀번호를 통해 새롭게 암호화하여 저장합니다.  
          </div>
          <div class="col s12 m4 l6 center">
            <img width="300" data-action="zoom" src='{{ "/assets/imgs/4_restore.png" | relative_url }}' alt='absolute'> 
          </div>
      </div>
</div>