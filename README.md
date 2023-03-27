# DART 학습용 프로젝트

본 프로젝트는 flutter를 학습하기 위한 dart 학습용 프로젝트입니다.

## 0. 개요

dart는 구글에서 개발한 객체지향 프로그래밍 언어입니다.

기본적으로 dart는 main 함수를 자동으로 실행합니다.

포메터가 자동으로 세미콜론을 붙여주지 않기 때문에, 세미콜론을 붙여주는 습관을 들이는 것이 좋습니다.

## 1. 변수

1. var

var 키워드를 사용하여 **변수를 선언**할 수 있습니다.

var 키워드는 관습적으로 함수 또는 메소드의 지역변수를 선언할 때 사용합니다.

그 외 클래스 또는 프로퍼티의 경우에는 타입을 명시해주는 것이 좋습니다.

2. dynamic

dynamic 타입은 **모든 타입을 허용**합니다.

```dart
void main() {
  var name;
  name = 'John';
}
```

```dart
void main() {
  dynamic name;
  name = 'John';
}
```

3. null safety

null safety는 TypeScript의 **strict mode**와 같은 개념입니다.

변수를 선언할 때 타입 뒤에 ?를 붙여주면 null을 허용합니다.

```dart
void main() {
  String? name;
  name = null;
  if(name != null) {
    name.isNotEmpty;
  }
  // name?.isNotEmpty;
}
```

4. final

final 키워드는 **한 번 값을 할당하면 변경할 수 없는** 상수입니다.

JavaScript의 const와 유사합니다.

```dart
void main() {
  final name = 'John';
  // name = 'Doe';
}
```

5. late

late 키워드는 변수를 **선언할 때 값을 할당하지 않고**, 나중에 할당할 수 있습니다.

```dart
void main() {
  late final String name;
  name = 'John';
}
```

6. const

const 키워드는 **컴파일 시점**에 값을 할당해야 합니다. (런타임 시점에 값을 할당할 수 없습니다.)

```dart
void main() {
  const name = 'John';
  // name = 'Doe';
}
```

## 2. 데이터 타입

dart에서 모든 데이터 타입은 객체입니다. (class로 구현되어 있습니다.)

1. String

```dart
void main() {
  String name = 'John';
  String name2 = "John";
  String name3 = '''John''';
  String name4 = """John""";
}
```

2. int

```dart
void main() {
  int age = 10;
  int age2 = 0x10;
  int age3 = 0b10;
  int age4 = 0x10;
}
```

3. double

```dart
void main() {
  double height = 10.0;
  double height2 = 10;
}
```

4. num

```dart
void main() {
  num age = 10;
  num height = 10.0;
}
```

5. bool

```dart
void main() {
  bool isTrue = true;
  bool isFalse = false;
}
```
