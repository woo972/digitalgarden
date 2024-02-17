---
{"dg-publish":true,"permalink":"/Gradle 빌드 시 특정 디렉토리 포함하거나 제외하기/","tags":["dev","gradle"],"noteIcon":""}
---


```kotlin
sourceSets {  
    main {  
        kotlin {  
            exclude("**/mock/**/*")  
        }  
    }    
    test {  
        kotlin {  
            include("**/mock/**/*")  
        }  
    }
}
```
위와 같이 설정하면 mock 패키지 하위에 속한 모든 파일에 대해 테스트시에는 사용하면서 실제 빌드된 결과물에서는 제외할 수 있다