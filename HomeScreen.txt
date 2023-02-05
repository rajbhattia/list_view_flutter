// ignore_for_file: prefer_const_constructors

import 'package:flutter/material.dart';

class HomeScreen extends StatelessWidget {
  HomeScreen({super.key});
  List fruitnames = ['apple', 'banana', 'staberry', 'gauva'];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        centerTitle: true,
        title: Text('list view and grid vivew'),
      ),
      body: ListView(
        // ignore: prefer_const_literals_to_create_immutables
        children: fruitnames.map((e) => 
        Card(
           color: Colors.blue,
            child: Padding(
              padding: const EdgeInsets.all(15.0),
              child: Text(e),
            ),
          ),
        ).toList(),
      ),
    );
  }
}
