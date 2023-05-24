# Open-Source-Project
Open Source Project

## Hello My Name is MINSEUNG KANG
***My hakbun is 20192238 and third grade.

**My major is Computer Engeneering.

---
# 리눅스 top, ps, jobs, kill 명령어
## 1. top 명령어
#### 'top' 명령어는 시스템의 실시간 프로세스 모니터링을 제공하는 유용한 도구

#### 또한 CPU 메모리, 디스크 등의 시스템 리소스 사용 상황과 실행 중인 프로세스 목록 확인 가능
![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1731AC524E07FB5824)
#### 사용 예시
1. top 명령어 실행:
  터미널에서 top을 입력하고 엔터를 누르면 top 명령어가 실행되며, 실시간으로 시스템 정보가 업데이트된다. top 창이 열리고 CPU 사용률, 메모리 사용률, 실행 중인 프로세스 목록 등이 표시된다.
2. top 명령어 종료:
  top 명령어를 종료하려면 q 키를 누른다.

3. top 명령의 다양한 옵션:
    + 'd <초>': 화면을 갱신하는 주기를 설정한다.
    + -p <'PID'>: 특정 프로세스의 상태만 표시합니다. <'PID'>는 프로세스의 식별자를 나타냅니다.
    + '-u <사용자명>': 특정 사용자의 프로세스만 표시한다.
    + 'Shift + f' 또는 'f': 출력되는 정보의 정렬을 변경할 수 있는 메뉴를 표시한다.
    + 'Shift + o' 또는 'o': 현재 정렬 기준에 따라 프로세스 목록을 다시 정렬한다.
    + 'Shift + t' 또는 't': 프로세스 목록을 CPU 사용량 순으로 정렬한다.
    + 'Shift + m' 또는 'm': 프로세스 목록을 메모리 사용량 순으로 정렬한다.

더 다양한 정보 >> <https://koromoon.blogspot.com/2020/09/top.html>

---
## 2. ps 명령어
#### 현재 실행 중인 프로세스에 대한 정보를 보여주는 명령어
![image](https://ko.linux-console.net/common-images/linux-ps-command/ps-command.png)
#### 사용 예시
1. ps 명령어 실행:
  터미널에서 ps를 입력하고 엔터를 누르면 ps 명령어가 실행되며, 현재 실행 중인 프로세스 목록이 표시된다. 기본적으로는 현재 사용자에 대한 프로세스 목록만 표시된다.
2. ps 명령어 옵션:

    + '-e': 시스템 전체의 모든 프로세스를 표시한다.
    + '-f': 자세한 정보를 포함하여 프로세스 목록을 표시한다.
    + '-l': 긴 형식으로 프로세스 목록을 표시한다.
    + '-u <사용자명>': 특정 사용자의 프로세스만 표시한다.
    + '-p <'PID'>': 특정 'PID'에 해당하는 프로세스 정보만 표시한다.

더 다양한 정보 >> <https://jhnyang.tistory.com/268>

---
## 3. jobs 명령어
#### 쉘에서 실행 중인 백그라운드 작업의 목록을 보여주는 내장 명령어
![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F99B5DF505E60F42C10)

    'jobs': 현재 쉘에서 실행 중인 백그라운드 작업의 목록을 보여준다. 작업 번호(Job ID), 작업 상태, 작업에 할당된 프로세스 ID(PID) 등이 표시된다.
    '-l': 작업 목록을 자세한 형식으로 출력한다. 작업 번호, 작업 상태, 작업 시작 시간, 프로세스 그룹 ID, 작업 명령어 등이 표시된다.
    '-p': 쉘에서 실행 중인 작업들의 프로세스 ID(PID)를 출력한다. 

더 다양한 정보 >> <https://server-talk.tistory.com/434>
#### 주의할 점 : jobs 명령어는 현재 쉘 세션 내에서 실행 중인 작업들에 대해서만 정보를 제공한다. 만약 다른 쉘 세션에서 실행 중인 작업에 대한 정보를 확인하려면 해당 쉘 세션으로 이동하여 jobs 명령어를 실행해야 한다.

---
## 4. kill 명령어
#### 리눅스에서 프로세스를 종료시키는 명령어
#### kill 명령어를 사용하여 특정 프로세스에 종료 신호를 보내어 해당 프로세스를 강제로 종료시킬 수 있음
![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F99E84B455C6378A109)
#### 사용 예시
1. kill 명령어 실행:
  kill [옵션] <프로세스 ID>
2. kill 명령어 옵션:
      + '-s <시그널>': 특정 종료 시그널을 지정한다. 기본적으로 kill 명령어는 SIGTERM 신호를 보내어 프로세스를 종료시킨다. 일부 자주 사용되는 시그널은 SIGKILL (-9), SIGINT (-2), SIGSTOP (-19) 등이 있다. 예를 들어, kill -9 <프로세스 ID>는 프로세스를 강제로 종료시킨다.
      + '-l': 사용 가능한 종료 시그널 목록을 표시한다.

더 다양한 정보 >> <https://veneas.tistory.com/entry/Linux-%EB%A6%AC%EB%88%85%EC%8A%A4-%EC%8B%9C%EA%B7%B8%EB%84%90-%EB%AA%85%EB%A0%B9%EC%96%B4%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%EC%A2%85%EB%A3%8C-kill>
#### 주의할 점 : 강제로 종료하는 경우 프로세스가 작업을 정리하지 못할 수 있으므로 데이터 손실이 발생할 수 있다.

| 명령어 | 옵션 |
|:---:|:---:|
| top | d,p,u ... |
| ps | e, f, l, u, p ... |
| jobs | l, p .. |
| kill | s, l .. |
