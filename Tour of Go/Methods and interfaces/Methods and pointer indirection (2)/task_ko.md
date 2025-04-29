# 메서드와 포인터 간접 참조 (2)

반대 방향에서도 동일한 일이 발생합니다.

값 인수를 받는 함수는 반드시 해당 특정 타입의 값을 받아야 합니다:

	var v Vertex
	fmt.Println(AbsFunc(v))  // OK
	fmt.Println(AbsFunc(&v)) // 컴파일 오류!

반면, 값 리시버를 가진 메서드는 호출될 때 값이나 포인터를 리시버로 받을 수 있습니다:

	var v Vertex
	fmt.Println(v.Abs()) // OK
	p := &v
	fmt.Println(p.Abs()) // OK

이 경우, 메서드 호출 `p.Abs()`는 `(*p).Abs()`로 해석됩니다.