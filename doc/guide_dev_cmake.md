# CMake 가이드라인
libnghttp2_asio

Make에 대한 이해. 
https://www.gnu.org/software/make/manual/make.html#Reading 

make에게 알릴 "makefile"라는 파일이 필요하다. makefile은 대게 make에게 어떻게 컴파일할지와 프로그램 링크에 대한 것을 담고 있다. 
.am 파일은 무엇에 쓰는고?

makefiledms "규칙들"로 이루어져 있다. 
```
target ... : prerequisites ...
          recipe
          ...
          ...
```

1. target: 프로그램에 의해 생성될 파일을 의미; 실행 파일이나 오브젝트 파일.
2. prerequisite: target을 생성할 때 필요한 입력으로 사용됨;
3. recipe: make가 실행할 하나 이상의 행동(최소 단위의 명령어)
4. rule: 어떻게 언제 특정 규칙을 바탕으로 target을 수행할 지 설명;

Phony Targets
이는 실제 파일의 이름이 아니며, 명시적으로 make에 요청할 때 수행되는 방법을 위한 이름이다. 동일한 이름의 파일 사용을 피하고 퍼포먼스를 향상하기 위해 사용

SUBDIRS
재귀적으로 make를 수행하기 위해 SUBDIRS = {폴더이름} {폴더이름} ... 띄어쓰기 구분자로 두어 지정할 수 있다

