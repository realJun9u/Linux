### fdisk / parted

fdisk - 2TB 이하의 MBR(Master Boot Record)

parted - 2TB 이상의 GPT(Guid Partition Table)

### 리눅스 파일 시스템

ext - 초기 리눅스에서 사용하였던 종류, 현재는 사용하지 않음

ext2 - 현재도 사용하며, 긴 파일시스템 이름을 지원하는 것이 특징

ext3 - 저널링 파일시스템, ext2보다 파일시스템의 복수/보안 기능이 크게 향상

ext4 - 16TB까지만 지원하던 ext3과는 달리 더 큰 용량을 지원하며, 삭제된 파일 복구,

   파일 시스템 속도가 훨씬 빨라진 파일시스템
```
- 1EB의 최대 파일 시스템 크기와 16TB의 크기의 파일을 지원

- 서브 디렉토리를 64000개 지원, 파일은 약 40억개 저장 가능

  TB → PB (페타) → EB (엑사)
```

swap - swap공간으로 사용되는 파일 시스템

xfs - 64bit 고성능 저널링 파일 시스템

iso9660 - DVD/CD-ROM을 위한 표준 파일 시스템으로 읽기만 가능

nfs - 원격 서버에서 파일 시스템 마운트 할 때 사용하는 시스템 (Network File System)

### Hard Disk 종류 

- IDE (Integrated Drive Electronics)

- SATA (Serial Advanced Technology Attachment)

- SCSI (Small Computer System Interface)

- SAS (Serial Attached SCSI) 크기가 작고 빠르며, 안정적이다. → 가격이 비싸다

디스크가 추가될 때마다 문자가 알파벳순으로 증가

/dev/sda → 첫 번째 디스크

/dev/sdb → 두 번째 디스크

/dev/sdc → 세 번째 디스크
 
#### 파티션 (Parition)

하나의 물리적인 디스크를 여러개의 논리적인 디스크로 나누는 것

리눅스 파티션 명칭

/dev/sda1 → 1번 디스크의 1번 파티션 

/dev/sda2 → 1번 디스크의 2번 파티션
