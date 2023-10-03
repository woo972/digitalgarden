---
{"dg-publish":true,"permalink":"/03.Resources/Dev/Flutter/Flutter- Web에서 Test해보기/","tags":["dev","flutter"],"noteIcon":""}
---



DartPad([https://dartpad.dartlang.org/](https://dartpad.dartlang.org/))에서 web관련 package import하여 flutter 테스트 가능

```dart
import 'package:flutter_web/material.dart';
import 'package:flutter_web_ui/ui.dart' as ui;

class MyApp extends StatelessWidget {
	@override
	Widget build(BuildContext context) {
		return MaterialApp(
			home: Scaffold(
			body: Center(
				child: Text('Hello world'),
				),
			),
		);
	}
}

Future<void> main() async {
	await ui.webOnlyInitializePlatform();
	runApp(MyApp());
}
```