## Laboratory work XV

Данная лабораторная работа посвещена изучению инструментов статического и динамического анализа кода
```ShellSession
$ open http://cppcheck.sourceforge.net
```

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Используя **cpplint** провести анализ проекта на **C++**
- [x] 3. Используя **Cppcheck** провести анализ проекта на **C++**
- [x] 4. Используя **OCLint** провести анализ проекта на **C++**
- [x] 5. Используя **Valgrind** провести анализ проекта на **C++**
- [x] 6. Составить отчет и отправить ссылку личным сообщением в **Slack**

```ShellSession

$ cpplint hello.cpp
Done processing hello.cpp

$ cppcheck hello.cpp
Checking hello.cpp...

$ oclint hello.cpp -- -c


OCLint Report

Summary: TotalFiles=1 FilesWithViolations=0 P1=0 P2=0 P3=0 


[OCLint (http://oclint.org) v0.13]

$ cmake -H. -B_builds 
$ cmake --build _builds
$ cd _builds

$ valgrind ./hello
==2434== Memcheck, a memory error detector
==2434== Copyright (C) 2002-2015, and GNU GPL'd, by Julian Seward et al.
==2434== Using Valgrind-3.11.0 and LibVEX; rerun with -h for copyright info
==2434== Command: ./hello
==2434== 
Hello, world!
==2434== 
==2434== HEAP SUMMARY:
==2434==     in use at exit: 72,704 bytes in 1 blocks
==2434==   total heap usage: 2 allocs, 1 frees, 73,728 bytes allocated
==2434== 
==2434== LEAK SUMMARY:
==2434==    definitely lost: 0 bytes in 0 blocks
==2434==    indirectly lost: 0 bytes in 0 blocks
==2434==      possibly lost: 0 bytes in 0 blocks
==2434==    still reachable: 72,704 bytes in 1 blocks
==2434==         suppressed: 0 bytes in 0 blocks
==2434== Rerun with --leak-check=full to see details of leaked memory
==2434== 
==2434== For counts of detected and suppressed errors, rerun with: -v
==2434== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

```
