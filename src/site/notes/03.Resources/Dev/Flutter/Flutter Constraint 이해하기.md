---
{"dg-publish":true,"permalink":"/03.Resources/Dev/Flutter/Flutter Constraint 이해하기/","tags":["flutter","dev"],"noteIcon":""}
---

'어떤' 위젯들은 그 크기와 포지션을 스스로 결정하지 못하고 부모 위젯에 의존한다.
기본적으로 부모 위젯으로부터 한계값을 받아, 해당 한계치 내에서 자식 위젯(들)의 사이즈, 포지션을 확인한 후에 부모위젯에 자신의 한계값과 사이즈를 알려주고, 부모위젯이 해당 위젯의 사이즈와 포지션을 결정하게 된다.

