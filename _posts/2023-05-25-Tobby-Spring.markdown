---
layout: post
title: Tobby Spring - 불필요한 의존관계 분리
date: 2023-05-25 17:50:30 +0300
description: Tobby Spring에서 DAO의 확장과 Class를 분리해주는 Interface도입으로 불필요한 의존관계를 개선하는 작업을 실시함  # Add post description (optional)
img: tobby-spring.jpg # Add image post (optional)
fig-caption: Tobby Spring # Add figcaption (optional)
tags: [study, tobbyspring]
permalink: 'post/tobbyspring'
comments: true
---

>Tobby Spring - 실습

* UserDao 클래스를 분리함
* UserDao 클래스는 SimpleConnectionMaker를 상속받아와 Connection을 할 수 있게 환경을 만듬
* 인터페이스 도입으로 추상화를 해놓아 최소한의 기능만 사용할 수 있도록 만듬
* 관계설정 책임의 분리임
* 관계설정 책임이 추가된 UserDao 클라이언트인 main method에서 DB Connection을 시도함

>Tobby Spring - 실습결과

![Tobyy Spring2]({{site.baseurl}}/assets/img/tobby-spring2.png)

>Tobby Spring - 실습후기

- DB의 보안성을 중요시 여기는 만큼, DB Connection을 외부에서도 사용을 할 수 있게 환경을 갖춰 분리작업과 해당 Class를 상속받고 Test환경에서도 문제없는지까지 실습하면서 흐름에 대해서는 이해를 하였고, Interface의 의미와 상속, 의존관계에 대해서도 배우다보니 조금은 이해가 되었고 특히 정리를 하면서 더 와닿는 것이 좋았고, 앞으로도 어떤 작업을 하더라도 상속에 있어 무조건적으로 호출하여 불필요한 관계를 줄여가고 의존관계로 개선하는 방향을 잡을 수 있도록 해야겠다는 생각이 들었음.