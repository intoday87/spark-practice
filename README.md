# spark-practice
spark를 배우면서 기억해놓아야할 내용들

# Hadoop
- 빅데이터 처리를 위한 분산 시스템 환경을 통칭
- spark와 마찬가지로 apache에서 같이 관리되고 있는 오픈소스
- HDFS(Hadoop Distributed File System)
  - scalablity, hardware failure를 극복하는 고가용성을 지원한다
  - master/slave 구조. master node는 metadata를 관리하고 slave node는 데이터 저장
- HDFS을 베이스로 yarn resource manager, map reduce 그리고 spark와 같은 어플리케이션이 올라가게 된다
