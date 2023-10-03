---
{"dg-publish":true,"permalink":"/03.Resources/Dev/Flutter/Flutter Error - Expanded widgets must be placed inside Flex widgets/","tags":["dev","flutter"],"noteIcon":""}
---


An Expanded widget must be a descendant of a Row, Column, or Flex, and the path from the Expanded widget to its enclosing Row, Column, or Flex must contain only StatelessWidgets or StatefulWidgets (not other kinds of widgets, like RenderObjectWidgets).

Expanded  내부에 [ListView.build](http://listview.build) 를 쓰는 경우에도 발생함