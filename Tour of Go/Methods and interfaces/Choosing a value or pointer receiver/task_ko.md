# 값 또는 포인터 리시버 선택

포인터 리시버를 사용하는 데는 두 가지 이유가 있습니다.

첫 번째는 메서드가 리시버가 가리키는 값을 수정할 수 있도록 하기 위해서입니다.

두 번째는 메서드 호출마다 값을 복사하는 것을 방지하기 위해서입니다.  
예를 들어, 리시버가 큰 구조체일 경우 이렇게 하면 더 효율적일 수 있습니다.

이 예제에서 `Scale`과 `Abs`는 모두 리시버 타입이 `*Vertex`인 메서드입니다.  
`Abs` 메서드는 리시버를 수정할 필요가 없더라도 말입니다.

일반적으로, 특정 타입의 모든 메서드는 값 리시버 또는 포인터 리시버를 가져야 하며, 두 가지를 혼용해서는 안 됩니다.  
(다음 몇 페이지에서 그 이유를 살펴보겠습니다.)