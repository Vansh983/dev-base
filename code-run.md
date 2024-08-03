# Programming Language Commands

## Overview
- [JavaScript](#javascript)
- [Python](#python)
- [TypeScript](#typescript)
- [Java](#java)
- [C](#c)
- [C++](#c-1)
- [C#](#c-2)
- [Go](#go)
- [Dart](#dart)
- [Kotlin](#kotlin)

## JavaScript

### Running a JavaScript File

To run a JavaScript file using Node.js:

```sh
node file-name.js
```

Replace `file-name.js` with the name of your JavaScript file.

## Python

### Running a Python File

To run a Python file:

```sh
python file-name.py
```

For Python 3.x, you might need to use:

```sh
python3 file-name.py
```

Replace `file-name.py` with the name of your Python file.

## TypeScript

### Running a TypeScript File

To compile a TypeScript file to JavaScript:

```sh
tsc file-name.ts
```

To run the compiled JavaScript file:

```sh
node file-name.js
```

Replace `file-name.ts` with the name of your TypeScript file and `file-name.js` with the name of the compiled JavaScript file.

## Java

### Running a Java File

To compile a Java file:

```sh
javac file-name.java
```

To run the compiled Java file:

```sh
java file-name
```

Replace `file-name.java` with the name of your Java file and `file-name` with the name of the compiled Java class.

## C

### Running a C File

To compile a C file:

```sh
gcc file-name.c -o output-name
```

To run the compiled C file:

```sh
./output-name
```

Replace `file-name.c` with the name of your C file and `output-name` with the name of the output file.

## C++

### Running a C++ File

To compile a C++ file:

```sh
g++ file-name.cpp -o output-name
```

To run the compiled C++ file:

```sh
./output-name
```

Replace `file-name.cpp` with the name of your C++ file and `output-name` with the name of the output file.

## C#

### Running a C# File

To compile and run a C# file using the .NET CLI:

```sh
dotnet new console -o MyApp
cd MyApp
dotnet run
```

Replace `MyApp` with the name of your project directory.

## Go

### Running a Go File

To run a Go file:

```sh
go run file-name.go
```

To build and run a Go file:

```sh
go build file-name.go
./file-name
```

Replace `file-name.go` with the name of your Go file.

## Dart

### Running a Dart File

To run a Dart file:

```sh
dart file-name.dart
```

Replace `file-name.dart` with the name of your Dart file.

## Kotlin

### Running a Kotlin File

To compile and run a Kotlin file:

```sh
kotlinc file-name.kt -include-runtime -d file-name.jar
java -jar file-name.jar
```

Replace `file-name.kt` with the name of your Kotlin file and `file-name.jar` with the name of the output JAR file.