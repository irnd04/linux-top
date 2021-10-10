# linux-top

```
top - 08:37:08 up 4:53, 2 users, load average: 0.21, 0.31, 0.19
```
* `08:37:08` 해당 결과를 본 시간을 의미. 현재의 시스템 시간
* `up 4:53` 시스템이 시작해서 지금까지의 시간, 즉 uptime을 의미
* `2 users` 터미널을 통하여 시스템에 접근한 사용자 세션의 개수
* `load average` 왼쪽부터 1분, 5분, 15분의 부하 평균값을 제공. 

```
Tasks: 134 total, 1 running, 132 sleeping, 0 stopped, 1 zombie
```
* 수행 중인 작업들의 통계를 나타냄
* `total`은 전체 수행 중인 프로세스의 수
* `running` 수행 중
* `sleeping` 대기 중
* `stopped` 종료
* `zombie` 좀비

```
%Cpu(s):  0.3 us,  0.9 sy,  0.0 ni, 98.8 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
KiB Mem :  8124336 total,  1368676 free,  3320184 used,  3435476 buff/cache
KiB Swap:  1942896 total,  1942896 free,        0 used.  4470936 avail Mem 
```
* 위 3개의 라인은 linux-troubleshooting 참고

항목 | 내용
-- | --
PID | 프로세스 아이디
USER | 해당 프로세스를 수행한 사용자의 아이디
PR | 작업의 우선순위
NI | 작업의 nice값. 값이 음수일 경우에는 매우 높은 우선순위를 뜻함.
VIRT | 작업에서 사용한 가상 이미지를 사용한 크기(KB). VIRT=RES+SWAP
RES | 점유한 메모리 크기, 스왑된 부분은 제외
SHR | 공유 메모리 크기. 다른 프로세스와 공유할 수 있는 메모리의 크기
S | 프로세스의 상태. D(중단 불가능한 잠자기 상태), R(실행 중인 상태), S(잠자기 상태), T(트레이스되었거나 중지된 상태), Z(좀비상태)
%CPU | CPU 사용량
%MEM | 메모리 사용량
TIME+ | 프로세스가 CPU를 점유한 시간의 누적값
COMMAND | 작업을 수행한 명령어

