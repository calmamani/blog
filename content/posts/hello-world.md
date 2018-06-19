---
title: "Hello World In Several Languages"
date: 2018-06-19T10:58:56+03:00
---

## Assembly x64

```
; Define variables in the data section
SECTION .DATA
    hello:    db 'Hello world!',10
    helloLen: equ $-hello

; Code goes in the text section
SECTION .TEXT
	GLOBAL _start 

_start:
	mov eax,4            ; 'write' system call = 4
	mov ebx,1            ; file descriptor 1 = STDOUT
	mov ecx,hello        ; string to write
	mov edx,helloLen     ; length of string to write
	int 80h              ; call the kernel

	; Terminate program
	mov eax,1            ; 'exit' system call
	mov ebx,0            ; exit with error code 0
	int 80h              ; call the kernel
```

## Java

```
public class Hello {
    public static void main(String... args) {
    	System.out.println("Hello World!");
    }
}
```

## Scala

```
object Hello {
	def main(args: Array[String]): Unit = {
		println("Hello World!")
	}
}
```

## C

```
#include <stdio.h>

int main() {
	printf("Hello World!");

	return 0;
}
```


## C++

```
#include <iostream.h>
using namespace std;

int main() {
	cout << "Hello World!" << endl;
	return 0;
}

```

## Go

```
package main

import "fmt"

func main() {
	fmt.Println("Hello World!")
}

```

## Rust

```
fn main() {
	println!("Hello World!")
}
```

## JavaScript

```
(function(){
	"use strict";
	function hello() {
		console.log("Hello World!")
		alert("Hello World!")
	}
	hello();
})();
```

## Python

```
print("Hello World!")
```

## Julia

```
println("hello world")
```

## Bash

```
echo "Hello World!"
```

## PHP

```
<?php
echo("Hello World!");
?>
```
