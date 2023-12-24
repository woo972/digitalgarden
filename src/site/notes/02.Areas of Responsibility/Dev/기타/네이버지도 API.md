---
{"dg-publish":true,"permalink":"/02.Areas of Responsibility/Dev/기타/네이버지도 API/","tags":["map","api","naver","dev"],"noteIcon":""}
---

#### 지도 실행
```
nmap://map?&appnamne=com.example.app
```
웹에서 실행시 nmap://map 으로도 가능
#### 지도 검색
```
nmap://search?query=<encoded search keyword>
```
#### 마커 표시
```
nmap://place?lat=<lat>&lng=<lng>&name=<name>
```
#### 길찾기
- 대중교통
```
nmap://route/public
```
- 차
```
nmap://route/car
```
- 도보
```
nmap://route/walk
```
##### 파라미터
| 변수명 | 타입   | 필수여부 | 설명         |
| ------ | ------ | -------- | ------------ |
| slat   | double | N        | 출발지 위도  |
| slng   | double | N        | 출발지 경도  |
| sname  | string | N        | 출발지 이름  |
| dlat   |        | Y        |              |
| dlng   |        | Y        |              |
| dname  |        | N        |              |
| v1lat  |        | N        | 경유지1 위도 |
| v1lng  |        | N        | 경유지1 경도 |
| v1name |        | N        | 경유지1 이름 |
** 경유지는 총 5개까지 가능


