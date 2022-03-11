# hive_test

A new Flutter project.

## Getting Started
 - Install dependencies
    dependencies:
  hive: ^[version]
  hive_flutter: ^[version]

dev_dependencies:
  hive_generator: ^[version]
  build_runner: ^[version]

  - flutter pub add hive
  - flutter pub add hive_flutter
  - flutter pub add -d hive_generator
  - flutter pub add -d build_runner

- Create a class 'user.dart' and put data like this

import 'package:hive/hive.dart';

part 'user.g.dart';

@HiveType(typeId: 1)
class User {

  User({required this.name, required this.age});

  @HiveField(0)
  String name;

  @HiveField(1)
  int age;
}

- Run this command to generate Adapter 

flutter packages pub run build_runner build



