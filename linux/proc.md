## proc는 가상의 파일 시스템입니다.
* 프로세스의 메모리 사용량 및 소켓의 현재 지표를 리눅스의 철학인 '모든 것은 파일이다.' 라는 철학에 맞춰 파일 시스템의 형태로 프로세스의 정보를 제공합니다.
* proc의 구조는 기본적으로 이런 정보를 제공하고 있었습니다.
<img width="484" height="387" alt="image" src="https://github.com/user-attachments/assets/c763533b-b718-476a-a60a-881517f804d4" />

저에게 가장 익숙한 tcp 소켓의 정보와 메모리 사용량을 보기로 결정했습니다.

### 소켓
<img width="1346" height="420" alt="image" src="https://github.com/user-attachments/assets/0a55cdbd-8aa2-411f-80b6-74247a8d5826" />

* netstat는 proc에 있는 정보를 보고 만드는 것 이었습니다.
* 역시 소켓도 파일이라서 inode의 정보가 포함되어 있었습니다.


그것 때문에 ss -t 로 커널에 요청에 보내는 것 보다 오버헤드가 심하다고 합니다.

### 메모리 
<img width="308" height="428" alt="image" src="https://github.com/user-attachments/assets/b1d43430-2d99-4118-8aa7-1596fb52af36" />
* 메모리 사용량이 한눈에 보입니다.
* 프로세스에 관한 메모리 사용량을 모니터링 하면 top이 더 좋을 것 같습니다.
