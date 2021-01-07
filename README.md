# spark-practice
spark를 배우면서 기억해놓아야할 내용들

# Hadoop
- 빅데이터 처리를 위한 분산 시스템 환경을 통칭
- spark와 마찬가지로 apache에서 같이 관리되고 있는 오픈소스
- HDFS(Hadoop Distributed File System)
  - scalablity, hardware failure를 극복하는(fault tolerence) 고가용성을 지원한다
  - master/slave 구조. master node는 이중화되어 metadata를 관리하고 slave node는 multiple data node로 데이터 저장
  - 데이터는 block단위로 복제되어 여러 노드에 저장되기 때문에 fault tolerence가 가능
  - default block 사이즈는 최근에 128mb
- HDFS을 베이스로 yarn resource manager, map reduce 그리고 spark와 같은 어플리케이션이 올라가게 된다
- map reduce(MR)는 대상 노드에서 map 함수로 추출하고 다른 노드에서 정렬 및 병합해서 분산 노드에서 결과를 도출하는 방식
  - **spark도 map reduce 모델을 기반으로 만들어졌다**

# Spark
- cluster computing에서 map reduce보다 디스크 기준 10배 메모리 기준 100배 빠르다
- United Computing Engine and a Set of library for Parallel Data Processing on Computer Cluster
- low level RDDs, Distribute Varabile을 기반으로 구조화됨
- MR vs Spark
  - MR은 map에서 얻어진 결과를 다시 hdfs에 씀. 읽고 쓰고를 반복해서 성능이 떨어짐
  - Spark은 점점 더 가격이 저렴해지는 메모리를 기반으로 처리 결과를 저장함 
 - scalar 언어로 구현됨
 - spark streaming으로 실시간 스트리밍 가능

## Basic Architecture
- todo: driver, session, executors(실제 일을 하는)

## DataFrame
- schema가 있는 데이터 처리

## When not to use
- SQL에 최적화된 DB 대체는 
