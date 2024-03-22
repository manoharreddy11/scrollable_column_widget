import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  final List<String> items = List.generate(50, (index) => 'Item ${index + 1}');

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Scrollable Column Example'),
        ),
        body: SingleChildScrollView(
          child: Center(
            child: Column(
              children: items.map((item) => Text(item)).toList(),
            ),
          ),
        ),
      ),
    );
  }
}
